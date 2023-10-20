# NotSoBot custom tag: Server Bulletin Board

**Server Bulletin Board (bboard)** is a custom NotSoBot tag that allows members of a Discord server to write plain black text messages on a blank HTML page, essentially creating a virtual bulletin board.

The project was made on my spare time and it took about 15 hours of work (including figuring out how to make NotSoBot make a damn HTTP request), I'm an 18-year-old novice programmer currently about to graduate a tech-oriented high school.

The tag makes use of, as far as I know, the only way for a NotSoBot tag script to make an HTTP request, through the use of the bot's own custom language intended for image manipulation "iscript" it uses the screenshot command to make the bot enter the website (thus triggering its server-side scripts) and screenshot it, NotSoBot then posts said image.

## Important Considerations Before Setting Up

- Please note that the project stores data in JSON files instead of a MySQL database, which are easily accessible via a web browser. However, the data stored does not compromise users' privacy, for it only stores the Discord user IDs of those who have used the tag at least once (in order to keep track of votes and 10 second cooldown) and the messages in the bulletin board.
- Due to limitations in NotSoBot and in myself, be aware that the code could be vulnerable to hijacking. I believe the consequences are limited to the JSON files being wiped from the server but I don't *really* know, host at your own risk.
- Quite often NotSoBot returns a MediaScript timeout error, that is an iscript bug, its out of my control, but do know that it means the HTTP request did go through (So if you wrote a message or voted to reset, it was stored)

## Set-up

1. If you don't have one, host an online website. In case you don't have a server or the money to pay for one, I personally used www.000webhost.com for my server's bulletin board, but be careful with those sketchy free web hosting websites. I'll be doing the rest of the setup in this website
2. Download the latest release for this project (The .zip file) and unzip
3. After unzipping, open the "start.nsb" file with any text editor and replace both "[YOURWEBSITE]"s with your website's URL, to whichever path you left the bboard folder in (Ej: coolserver.000webhostapp.com)
4. If you want to change the N° of how many people it takes to reset the board, you'll have to edit the file bboard/model/Functions.php, go to line 43 and change the "5" with whatever number, I'll make a more convenient way of doing this later lol
5. Upload the bboard folder to your web server. If you're using 000webhost, go to "File Manager" and upload it to the public_html folder (or any subdirectory)
![BBoardfolder](https://media.discordapp.net/attachments/1089617879122587660/1164740588525080596/image.png?ex=65445034&is=6531db34&hm=796e47a6552bac7d07adbcd21290fbb35c631ea5ecf6447bb956021b2ccfbcd7&=)
6. Copy and paste the contents of "start.nsb", go to the discord server of your choice and run the notsobot command "-t create bboard (code)"
![Message](https://media.discordapp.net/attachments/1089617879122587660/1164736519957921923/image.png?ex=65444c6a&is=6531d76a&hm=9d75bd387cc36f862c7ac4a31e61bc88325ee52a8ea2b3819f3e456627b272c3&=)
7. If the command is not working you typed the wrong URL in "[YOURWEBSITE]", note that you shouldn't type the "public_html" in the directory

## Demonstrations
![demo1](https://cdn.discordapp.com/attachments/1089617879122587660/1164744045961158676/image.png?ex=6544536c&is=6531de6c&hm=59ad5162edc0d871900e71e41a923fbb90468870941a69f37d51167875c7a82d&)
![demo2](https://cdn.discordapp.com/attachments/1089617879122587660/1164744235879247993/image.png?ex=65445399&is=6531de99&hm=aa337f7f552ef912bd9a3f5002ea932c820540d1be42726a73911dda76275324&)
![demo3](https://cdn.discordapp.com/attachments/1089617879122587660/1164744421682724884/image.png?ex=654453c6&is=6531dec6&hm=2a7fb0cf376e547d794e2de533240ec8c68602e6a86edfd25be80a72f9b37ebe&)

---

Feel free to contribute to this project or report any issues. There's probably many things wrong, have fun! :smiley:
