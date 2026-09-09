## Enumeration — Nmap

I started with an Nmap scan to identify open ports and running services.

nmap -sC -sV <TARGET_IP>




The scan revealed SMB-related services, which indicated that SMB enumeration could be useful.

## SMB Enumeration

I enumerated the SMB service and investigated the available shares/services.

smbclient -L //<TARGET_IP>/ -N




## Responder

The next step was to capture an authentication request in the HTB lab environment using Responder.

sudo responder -I tun0




Responder captured an NTLMv2 challenge-response hash.

The captured hash is omitted from this public writeup.

## Hash Cracking

I saved the captured hash to a file and used John the Ripper with the appropriate wordlist.

john --wordlist=<WORDLIST> hash.txt

To display the recovered password:

john --show hash.txt





## Remote Access

Using the recovered credentials, I obtained access to the Windows machine through the appropriate remote service.




## Flag

After gaining access, I enumerated the user's files and located the flag.

type <path-to-flag>
