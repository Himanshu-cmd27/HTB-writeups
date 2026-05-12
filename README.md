# HTB-writeups
Collection of Hack The Box (HTB) and TryHackMe machine writeups covering enumeration, exploitation, privilege escalation, and cybersecurity learning notes.
# Meow - Hack The Box (Starting Point)

## Objective
The goal of this machine was to gain initial access and retrieve the flag using basic enumeration.

---

# Enumeration

First, I performed a network scan using Nmap to identify open ports and services:

```bash
nmap -sV <IP>
```

### Result:
- Port 23 open (Telnet service detected)

---

##  Gaining Access

Since Telnet service was open, I connected to the target using:

```bash
telnet <IP>
```

No authentication was required, and I successfully gained access to the system.

---

## Flag Retrieval

After logging in, I explored the system and located the flag file.

Using:

```bash
ls
cat flag.txt
```

I retrieved the flag successfully.

---

# Key Learnings
- Basic network enumeration using Nmap
- Understanding Telnet service and its risks
- Importance of disabling insecure services like Telnet
