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

[Linux Mint User Guide](https://linuxmint-user-guide.readthedocs.io/_/downloads/en/latest/pdf/) :Hop over to the Chapter 6 to follow whatever i had said in this repo.

######  _4.what if i forgot the root passwd ?_
-I actually forgotten the root passwd and in the event of forgetting the root passwd you can't even get back your username and change your passwd .This video saved my time and energy [Linux Mint Video showing how to overwrite root password](https://youtu.be/8W5CWhg19pI?si=Hq5rFaVmfPqSi9Pu) .So you first restart your computer and then continuously press shift to get the grub menu .After that,select the Advanced options < Recovery mode. Instead of pressing recovery mode, you can usually do this,if you remember you root passwd.If not,then do not press the recovery mode instead press `e `(which stands for edit) and then scroll down until you see _linux_ and then go the last line of _linux_ and write this.
```
init=/bin/bash
```
After that press `fn+f10`
After that you need to write this command in the terminal:
```
mount -n -o remount,rw /
```
And then, Press `enter`
```
exec /sbin/init 
```
Again, Press `enter`

Afterwards you can reset your root passwd,by the following command:
```
passwd root
```
And then,you can hop over to the Advanced options < Recovery mode  then press `Enter`
And then hop over to **root** and enter you root passwd .
If you forgot your username then type:
```
ls /home
```
Afterwards type this:
```
passwd username
```
You should by now ,resetted the passwd and then restart your computer and enjoy your new passwd!







