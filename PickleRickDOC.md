# Pickle rick write up

Start by scanning ports using nmap (network mapper) to scan its open ports and services 
Ive used 

```nmap -p- -sV```
-p- meaning ports 
-sV port version 
with the ip address


![scanport](img/scanport.png)

Lets see the website

![web](img/web.png)

Use Ctrl+u to see source code there we can find what looks like a username R1ckRul3s

![username](img/username.png) 

To find the directories and files we are using ffuf

-u is the target URL
-w is the path to the wordlist files 
FUZZ we put this after the URL
-e parameter suffix to your wordlist (not all extensions start with a .)
-t threads or processes

![ffuf](img/ffuf.png)
![directories](img/directories.png)

We find robots.txt  

![robot.txt](img/robots.txt%20.png)

Containing Wubbalubbadubdub it looks like a password

Go to login.php enter Username: R1ckRul3s 
Password: Wubbalubbadubdub 

![login.php](img/login.php.png)

At the command panel start with ls 

![commandpanel](img/comandpanel.png)

Im going to try reading the file Sup3rS3cretPIckl3Ingred.txt

![failcat](img/failcat.png)

not working lets try instead a similar command 'tac'  


![tacIngred](img/tacIngred.png)

Result : mr meeseek hair

Lets look at one of the files

![clue.txt](img/clue.txt.png)

Attempt ls /home/ where the users are located

![home](img/home.png) 

Lets see inside /home/rick

![rickhome](img/rickhome.png)

tac home/rick/''second ingredients'' 
Remember to write in quotation marks if not it will read **second only** and as a directory.

![scondingred](img/secondingred.png)

Result : 1 jerry tear


Permissions sudo -l  

![sudo-l](img/sudo-l.png)

(ALL) NOPASSWD: ALL no password needed

Go to sudo ls /root/

![root](img/root.png)

sudo tac /root/3rd.txt 

![3rdingred](img/3rdingred.png)

Result : fleeb juice

Finished.