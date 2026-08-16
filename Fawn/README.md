# Fawn - Hack The Box
## 1. Enumeration
First i scanned the target IP using nmap to find open ports and service. then i found 21 open port and ftp running.
![Nmap Scan](fawnmap.png)
## 2. Ftp Enumeration
I connected to ftp service   
![FTP](ftp.png)

The server allowed anonymous login.
username : anonymous 
password : anonymous
After logging i listed the file using ls command 
and then found that file with name of 'flag.txt' then i downloaded it using get command 
## Flag
After that i opened it and got that flag 
