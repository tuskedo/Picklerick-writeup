# Pickle rick write up
Scan ports web

![scanport](img/scanport.png)

We can only read the website 

![web](img/web.png)

use Ctrl u to see source code there we can find R1ckRul3s

![username](img/username.png) 

To find the directories or files we are using ffuf

![ffuf](img/ffuf.png)
![directories](img/directories.png)

We find robots.txt containing Wubbalubbadubdub

![robot.txt](img/robots.txt%20.png)

Go to login.php enter user R1ckRul3s pass Wubbalubbadubdub 

![login.php](img/login.php.png)

At the command panel start with ls 

![commandpanel](img/comandpanel.png)

cat Sup3rS3cretPIckl3Ingred.txt 

![failcat](img/failcat.png)

not working try tac Sup3rS3cretPIckl3Ingred.txt result mr meeseek hair

![tacIngred](img/tacIngred.png)

tac clue.txt it reads Look around file system for the other ingridient 

![clue.txt](img/clue.txt.png)

Attempt ls /home/ shows rick

![home](img/home.png) 

ls /home/rick result second ingridients

![rickhome](img/rickhome.png)

then tac home/rick/''second ingredients'' 1 jerry tear

![scondingred](img/secondingred.png)

Permissions sudo -l  (ALL) NOPASSWD: ALL no password needed

![sudo-l](img/sudo-l.png)

Go to sudo ls /root/

![root](img/root.png)

sudo tac /root/3rd.txt fleeb juice

![3rdingred](img/3rdingred.png)

finished