Meow — Very Easy

Summary:
This box was not very hard we ping it then we use Nmap for scan and telnet for connection it is like most basic to understand....
it is one of the first box so it's main use is to understand the VPN we use to connect to target machine

Enumeration:
Upon Scan using Nmap we discovered that port 23/tcp is using telnet services 

Foothold:
I tried different login methods and got in just as with root and no password needed


Flags:
Hence after performing ls operations and searcing all files we find the flag 
/cat

What I Learned:
we can use ping to see if machine is up and scan it using the Nmap to map wht services are being used by the system and tried logging in with telnet and got in easily with root and no password
