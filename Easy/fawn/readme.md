Fawn — Very Easy

Summary
This box is about the remote ftp file transfer usually it uses port 21.
confirmed while scanning the machine

Enumeration
nmap -sV -p 21 [target-ip]

Scan showed port 21 open running an FTP service. Tried connecting with anonymous
login, a common misconfiguration where FTP servers allow login without real
credentials.

Foothold
Getiing in with ftp service command Ftp (ip_address)
and login with anonymous no password needed


Flags
Used `ls` to list files, found flag.txt, and used `get` to download it locally.
(Flag value omitted per HTB/THM guidelines.)

What I Learned
Ftp us a protocol allows file transfer from a remote server.
Anonymous login
enabled is a common misconfiguration which we can use to login without authentication
