now, here we go.  
start with using the same thing, except this time, open dbc.mpq and extract ChrRaces.dbc.

![[extractcp0.jpg]]

now use DBCUtil1 and drag the file onto it like with before. it should begin changing it, and on ur desktop or wherever u extracted it, u should see ChrRaces.dbc.csv  
  
now use CSVed and open up that file, then double click on any race on the opposite faction. this time im doing one for the horde, so lets double click on night elves, which is this.

![[csvednightelfhp3.jpg]]

now open notepad and label 1-30 in some way so u know which column is which. then write down in notepad what each column other than one says, if its blank, what i do is leave it blank, i do the same with number one considering that we will do nothing with column one. heres how it should look after u get through.(i just realised i accidently put in 4 on column one, just ignore that)

![[notepadfinishedlk0.jpg]]

now scroll down to orc and erase everything. u can recognise orc by seeing Orc in column 18. double click on that and erase everything u see besides column 1. then proceed to filling in the blanks with the data u collected. heres how it should look once u get through.

![[finishedot9.jpg]]

and there u go! just save it with file\save, then just drag the ChrRaces.dbc.csv back onto the DBCUtil1 program, and press enter to overwrite the origianal. now pack it back into a MPQ archive using MWS, and ur set! name the newly created file speech2 or patch-#(#being a number between 3-9), and add the file by putting DBFilesClient\ before the name of the file, so in our case it would be DBFilesClient\ChrRaces.dbc, and press ok. it should show as a folder and when u click the plus sign, it should have the file there. move it into ur data file and go into the game.  
  
ok, now many of u might not know what the title meant, it means u can whisper urself with whatever u wanna say to the horde or alliance, and then it will come across as whatever they see it as. im not sure if it is confermed working, but im pretty sure it works.  
  
From schlumpf:  
Clearification  
  
* you cant really talk to other factions or anything etc. it only changes it so you see yourself talking in that language ... to everyone else your talking your own normal language. (Cjizm)  
* it doesnt actually let u understand or anything thing, but it is usefull. put it in the data folder and log onto a changed char. then whisper urself whatever u want to say to the opposite faction, and it should come out with what to say. one thing though. u cannot say anything out loud, seriously. try typing something and attempt to /say it, and nothing will come out. so i would suggest writing down what it says, then exit and remove the file to speak normally again.  
  
the reason u would do this is to learn what certain words mean in the opposite language. but its like i said. but another reason u would do it is to get a full hold on what DBC editing can accomplish. its already been mentioned that u can edit flight paths and such, but think of all the other things. surely more than just this, and a few more things must be client side. for instance, location is client side, correct? areatriggers.dbc is what im thinking of. im trying to get people to branch out not just with this, but with all the database files. (Avianar47)

# Credits

- Avianar47