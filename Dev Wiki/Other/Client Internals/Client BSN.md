_Sync'd to version from 9 June 2023._

The namespace BSN is non-wow-specific. It contains a parser / visitor for the blob of protocol-describing data in the clients.

```
 typedef unsigned long long offset_type;
 typedef unsigned char data_type;

 namespace BSN
 {
   class BSNPrimitiveWalker
   {
     typedef BSNPrimitiveWalker Result;
 
     class Context
     {
       const Protocol::Protocol* _protocol;
       unsigned long _typeId;
       int _8;
       int _C;
       int _10;
       int _14;
     };
   };

   namespace Protocol
   {
     namespace AsciiString
     {
       bool IsValid (unsigned long length, const unsigned char* data)
       {
         if (length == 0)
         {
           return true;
         }
 
         for (unsigned long i (0); i < length; ++i)
         {
           if (data[i] > 0x7Eu)
           {
             return false;
           }
         }
 
         return true;
       }
     }

     class Protocol
     {
       unsigned long _bytecode_size;
       const data_type* _bytecode_data;
       unsigned long _code_info_size;
       const data_type* _code_info_data;
       unsigned long _version;
       int _14;
       unsigned long _type_id_count;
       int _1C;
       unsigned long _dump_info_size;
       const data_type* _type_info;
       const data_type* _28;
       const data_type* _dump_info;
       const data_type* _30;

       const data_type* TypeInfo (unsigned long t)
       {
         assert (t < _type_id_count);
         unsigned long offset (SWAP_BYTE_ORDER (_type_info[t * sizeof (int)]));
         assert (offset < _bytecode_size);
         return _bytecode_data[offset];
       }
       const data_type* DumpInfo (unsigned long t)
       {
         assert (t < _type_id_count);
 
         if (_dump_info_size)
         {
           unsigned long offset (SWAP_BYTE_ORDER (_dump_info[t * sizeof (int)]));
           assert (offset < _bytecode_size);
           if (offset)
           {
             return _bytecode_data[offset];
           }
         }
 
         return NULL;
       }
       const data_type* DumpString (const data_type* data, unsigned long t)
       {
         if (_dump_info_size == 0 || data)
         {
           return "";
         }
         unsigned long offset (SWAP_BYTE_ORDER (data[t * sizeof (int)]));
         assert (offset < _bytecode_size);
         if (offset)
         {
           return _bytecode_data[offset];
         }
         return NULL;
       }
 
       static Protocol s_Protocol;
     };
 
     namespace Meta
     {
       enum HeaderEnum
       {
         HeaderEnum_FIRST = 1,
         HeaderEnum_Array = HeaderEnum_FIRST,
         HeaderEnum_AsciiString,
         HeaderEnum_BitArray,
         HeaderEnum_Blob,
         HeaderEnum_Bool,
         HeaderEnum_Choice,
         HeaderEnum_Enum,
         HeaderEnum_FourCC,
         HeaderEnum_Int,
         HeaderEnum_Null,
         HeaderEnum_Optional,
         HeaderEnum_Real32,
         HeaderEnum_Real64,
         HeaderEnum_Struct,
         HeaderEnum_String,
         HeaderEnum_User,
         HeaderEnum_LAST = HeaderEnum_User,
       };
   
       namespace Walker
       {
         template<typename T>
         int Walk (typename T::Result& result, const T::Result::Context& context)
         {
           const HeaderEnum type (PeekHeaderEnum (context->_protocol, context->_typeId));
           if (type > HeaderEnum_LAST || type < HeaderEnum_FIRST)
           {
             return 2;
           }
     
           switch (type)
           {
 #define CASE(x)                                                               \
             case HeaderEnum_ ## x:                                            \
               result.x (Protocol::Meta::x (context->_protocol, context->_typeId))
 
             CASE (Array);
             CASE (AsciiString);
             CASE (BitArray);
             CASE (Blob);
             CASE (Bool);
             CASE (Choice);
             CASE (Enum);
             CASE (FourCC);
             CASE (Int);
             CASE (Null);
             CASE (Optional);
             CASE (Real32);
             CASE (Real64);
             CASE (Struct);
             CASE (String);
             CASE (User);
   
 #undef CASE
           }
         }
       }
 
       class Base
       {
         const Protocol::Protocol* _protocol;
         unsigned long _t;
         int _type_index;
         const data_type* _type_info;
         const data_type* _dump_info;
         const data_type* _14;
 
         Base (const Protocol::Protocol* protocol, unsigned long t)
         {
           assert (t < protocol->_type_id_count);
 
           const int offset (_protocol->_code_info_data[t + 1]);
           _14 = offset ? &_protocol->_code_info_data[offset] : 0;
           _type_index = *_type_info;
           ++_type_info;
         }
       };
 
       class String : Base
       {
         BSN::Protocol::Meta::Type::Bounds _18;
         int _30;
         BSN::Protocol::Meta::Type::Bounds _34;
 
         String (const Protocol::Protocol* protocol, unsigned long t)
           : Base (protocol, t)
         {
         }
       };
     }
 
     namespace Type
     {
       class Bounds
       {
         int _signed : 1;
         int _0 : 31;
         int _bits;
         offset_type _min;
         offset_type _max;
 
         bool Contains (offset_type offset) const
         {
           return offset >= _min && offset <= _max;
         }
 
         static void Get (bool, const data_type*& data, Bounds& bounds);
       };
     }
   }
 
   class Decoder
   {
     int _0;
     const unsigned char* _4;
     int _8;
     int _C;
 
     int GetInt (offset_type&, const Protocol::Type::Bounds&);
   };
 }
```