## Resetting the forgotten passwd in linux mint
#### **Description**

i forgot my linux mint both username and passwd after not logging in for many months and had not saved in any notes/password manager in my phone

#### **Solution**

###### _1.what help source did i took_
 -I took help from youtube,reddit..etc.
 ###### _2.what actually help me_
-Linux mint guide (user guide) that was freely available on the site...
###### _3.what the problem was really and how did i figure it out_

-Actually when i tried to brute force my to guess the password i couldn't remember it and when i tried following youtube tutorials and started entering the GRUB menu <advanced options< root but none help as i cannot get the correct username and in other sources of help for knowing the username it was showing (whoami)command which the result was root and definitely wasn't the right one ,and i tried multiple commands on my own like sudo passwd username(the one which was showing on the screen when i tried to log in)but that definitely wasn't the case, as i was on the verge of giving up, i remembered the room search skills in tryhackme where they taught the noobs,different ways to find the answer and to search like a pro(more specifically:google dorking),so i tried searching for the official pdf manual of linux mint guide and voila the command(ls /home)worked and i could successfully get back to my account. 

[Linux Mint User Guide](file:///C:/Users/chisa/Downloads/linuxmint-user-guide-readthedocs-io-en-latest.pdf)
