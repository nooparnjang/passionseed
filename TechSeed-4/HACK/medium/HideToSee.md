# HideToSee | medium - PicoCTF | Writeup
<h4>Hi this is my first writeup btw, so if i did anything wrong please feel free to tell me.</h4>

This is final project for **TechSeed camp #4**. I choose **"HideToSee""** just because the name. This challenges is cryptography which i love to solve like how fun they are. You can go solve [RightHere](https://play.picoctf.org/practice/challenge/351?page=1&search=Hidetosee)

<img width="954" height="688" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413129640486375506/image.png?ex=68bacf08&is=68b97d88&hm=bd21b556784511e88215cf01addda508ae0d2e857ca0d872c92948751cf46f3e&=&format=webp&quality=lossless&width=1193&height=860"/>

So i download the file and got this "atbash.jpg". btw there's nothing to do with 'RoyalOrderoftheHolyMackerel' i've already look it out.
<img width="750" height="75" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413129760242143242/atbash.jpg?ex=68bacf25&is=68b97da5&hm=69276bf531ebce5c0d3f218b2bd10936f5522186806d7fbcb712a5985b1cbf40&=&format=webp&width=581&height=569"/>

It's says atbash cipher that's mean it's a kind of cipher that encodes a message with the reverse of the alphabet, so east but where do i find the encode message.
So i use wget to download file in webshell 'cause i'm thinking of "strings".
<img width="1871" height="221" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413176889526194279/image.png?ex=68bafb0a&is=68b9a98a&hm=913b48818995ed42cf4165a57b48c8d647ce4664071e5f7a837ed8890c3fc5c0&=&format=webp&quality=lossless&width=1860&height=220"/>

Then i use strings with atbash.jpg and got this things. there's alot more that this but i'm tired.
<img width="427" height="879" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413176903585632326/image.png?ex=68bafb0d&is=68b9a98d&hm=7191b0b10dc9dadb33cd222e26f6143980ba5ce2ac3e499486bc31911c045930&=&format=webp&quality=lossless&width=451&height=929"/>

So as you see i could not read all of that, so i use grep to find what i want. I search for "{" like that's the start of flag. But there's nothing that's look like it's a flag that are encrypted with atbash cipher.

<img width="501" height="419" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413176920933400788/image.png?ex=68bafb11&is=68b9a991&hm=b5ca1ef05fa56997a9a0a23f2b61803244f37892db071afa0070bce0290bb1c9&=&format=webp&quality=lossless&width=626&height=524"/>

As i has come to the dead end, i click on the hint and got this hint "Download the image and try to extract it."
<img width="279" height="196" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413129654637695047/image.png?ex=68bacf0c&is=68b97d8c&hm=392d718eb042b58241667296fefdd7506a3252250f659861fae2d31cf26558f0&=&format=webp&quality=lossless&width=349&height=245"/>

So i as the very good listener i extract it in webshell using "steghide" (i've found this command by searching non-stop on google btw) then when i extract atbash.jpg i got the file "encrypted.txt" then i open encrypted.txt by using cat to read the file and then i got the flag yay!
<img width="1027" height="613" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413176929452032070/image.png?ex=68bafb13&is=68b9a993&hm=f78bc928593d03908dbcd690704b48fc79cde6fb8c25a77c8588e0261191b2d2&=&format=webp&quality=lossless&width=666&height=119"/>
**```krxlXGU{zgyzhs_xizxp_8z0uvwwx}```**

still not a real flag yet but we already got a clue from the atbash picture oc we have to use the atbash cipher. then i got the real flag!!
<img width="1027" height="613" alt="image" src="https://media.discordapp.net/attachments/1413129581472518295/1413184804840804361/image.png?ex=68bb0269&is=68b9b0e9&hm=07a8df15631ba8fae05b273d2acec9fa81239379b8320ce6a0d43c0209b60739&=&format=webp&quality=lossless&width=1284&height=766"/>
**```picoCTF{atbash_crack_8a0feddc}```**
## **PROBLEM SOLVE**
