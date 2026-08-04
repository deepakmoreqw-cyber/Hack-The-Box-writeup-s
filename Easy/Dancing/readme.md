Dancing — Very Easy

Summary
We learn about a SMB (Server Message Block) protocol which allows file sharing in a network we use -l for getting list of available smb share we get in in one on them without password easily.

Enumeration
It says to find service running on the port 445 so instead of full scan i do following command.

nmap -p 445 [ip_address]

                 service
port 445 open, microsoft-ds

Foothold
I used basic smbclient -L \\[ip_Address] to get list of available shares on our machine we attempt anonymous login in all of and found (WorkShares) which allows us access without credentials.

To actually connect to a share without a password, it's  smbclient \\[ip_address]\\sharename -N (the -N flag means "no password prompt"). 

Flags
After i get in with a SMB list withot password i simply used "ls" to see files available and at last after browsing through files and folders i got dancing/flag.txt 

flag.txt- location
"dancing/workshare/flag.txt."

What I Learned
I learned that smb i a protocol used to access files from another device in same network but we should be careful not to leave any file there which can be accessed without authentication.
