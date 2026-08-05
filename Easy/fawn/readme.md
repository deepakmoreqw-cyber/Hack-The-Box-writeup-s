Fawn — Very Easy

Summary: 
Fawn is an FTP-focused Very Easy box. FTP typically runs on port 21, which was confirmed during scanning.

Enumeration: 
nmap -sV -p 21 <target-ip> showed port 21 open, running an FTP service. Given this, I tried an anonymous login — a common FTP misconfiguration where the server accepts login without real credentials.

Foothold: 
Connected with ftp <ip-address> and logged in using anonymous with no password, which succeeded.

Flags: 
Used ls to list the directory contents, found flag.txt, and downloaded it locally with get. (Flag value omitted per HTB guidelines.)

What I Learned: 
FTP is a protocol for transferring files to/from a remote server. Anonymous login is a common misconfiguration that lets an attacker authenticate without valid credentials — worth checking on every FTP service you find
