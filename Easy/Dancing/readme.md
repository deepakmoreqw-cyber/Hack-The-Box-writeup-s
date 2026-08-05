Dancing — Very Easy

Summary: Dancing introduces SMB (Server Message Block), a protocol used for file sharing on a network. Using smbclient -L, we list the available shares on the target and find one accessible without a password.

Enumeration: The task pointed to SMB, which runs on port 445, so instead of a full scan I ran a targeted one:
nmap -p 445 <ip_address>
Result: port 445 open, running microsoft-ds.

Foothold: I used smbclient -L \\<ip_address> to list the available SMB shares and attempted anonymous login on each. One share, WorkShares, allowed access without credentials. To connect to it directly: smbclient \\<ip_address>\WorkShares -N (the -N flag skips the password prompt).

Flags: Once connected, I used ls to list available files, then browsed through the directories and found the flag at dancing/flag.txt.

What I Learned: SMB is used for sharing files/printers on a network and typically runs on port 445. Shares can sometimes be listed and accessed anonymously if misconfigured, which is a common initial foothold on easy boxes.

flag.txt- location
"dancing/workshare/flag.txt."

What I Learned
I learned that smb i a protocol used to access files from another device in same network but we should be careful not to leave any file there which can be accessed without authentication.
