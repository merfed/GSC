Ribbit is (an implementation of?) a new way of retrieving version information for products, with message verification via signatures (v1 only) and built-in caching. Uses sequence numbers returned by the summary (and every other request) to indicate whether something is outdated or not.

# Commands

Instead of using HTTP like the previous TACT system does, this uses a simple TCP socket. Commands are to be sent to either us.version.battle.net or eu.version.battle.net on port 1119 (ending in a \r\n). In this table, **bold** indicates a variable replaced in the actual query.

| Commands                    | Description                                                                 |
| --------------------------- | --------------------------------------------------------------------------- |
| v1/summary                  | Gets a list of endpoints and their current sequence number.                 |
| v1/products/product/version | Similar to TACT's version file, also referred to as version in other parts. |
| v1/products/product/cdns    | Similar to TACT's CDNs file, also referred to as CDN in other parts.        |
| v1/products/product/bgdl    | Similar to TACT's BGDL file.                                                |
| v1/certs/hash               | Get a certificate.                                                          |
| v1/ocsp/hash                | Check revocation status.                                                    |
| v1/ext                      | Unknown.                                                                    |
| v2/summary                  | See v1 summary and note on v2 message structure below.                      |
| v2/products/product/version | See v1 versions and note on v2 message structure below.                     |
| v2/products/product/cdns    | ***(NYI)*** See v1 CDNs and note on v2 message structure below.             |
| v2/products/product/bgdl    | See v1 BGDL and note on v2 message structure below.                         |

# Sequence Numbers

These can be found in every message and have been included in TACT HTTP requests since April 12 2018. Every time a file is updated the sequence number increases and the number in summary updates to let clients know that file has been updated. Sequence numbers never go down, if a lower one is detected that message/update can be treated as out of date. As such, rollbacks will also increase sequence numbers even though any other content in the file will go back to an older version.ᵛ

**Note:** As of June 10th 2022, sequence numbers returned by the summary and the endpoints themselves no longer match due to a change/issue on Blizzard's end. Summary seqns and endpoint seqns both still change when an endpoint changes but don't match.

# Cached Messages

Cached messages can be found in C:\ProgramData\Battle.net\Agent\data\cache. Filenames are structured like **command**-**argument(s?)**-**seqn**.bmime. If no arguments are present, argument in filename is #. If no seqn is present, it is 0.

**Examples**:

| Filename                                              | Description                                                                    |
| ----------------------------------------------------- | ------------------------------------------------------------------------------ |
| cdn-wow_beta-14722.bmime                              | Cached /cdns message for product wow_beta with sequence number 14722.          |
| summary-#-32324.bmime                                 | Cached /summary message with no arguments but with sequence number 32324.      |
| cert-5168ff90af0207753cccd9656462a212b859723b-0.bmime | Cached /cert message with certificate hash as argument and no sequence number. |

# Message Structure

## v1

V1 messages are [MIME](https://en.wikipedia.org/wiki/MIME) formatted and as such contain headers, boundaries (with content inside) and such.

One of the parts of the V1 message is always ASN.1 base-64 formatted data to ensure message validity and prevent MITM attacks. Each new update to a command's output yields a new base-64 chunk. While largely useless for our purposes, these are timestamped to their time of creation, giving exact time at which an update to a command was published (and thus when an update is rolled out). AN implementation of ASN.1 parsing in Javascript can be found [here](https://lapo.it/asn1js/).

Each V1 message ends with a SHA-256 checksum which is a checksum of all of the message except for the checksum line.

# v2

At time of writing (June 16th 2022) V2 messages only return actual content and don't contain any of the above metadata. V2 is still a WIP and this might change at a later date.

# Summary File

Similar to other TACT pipe (|) separated files. Contains a list of products/endpoints and their current sequence number. If the flags column is empty, it seems to refer to the version file. This file should be used to check for differences instead of checking all individual products like is currently done in HTTP TACT.