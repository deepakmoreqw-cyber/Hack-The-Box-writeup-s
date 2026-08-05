Meow — Very Easy

Summary: Meow is a very easy HTB machine and a good starting point for understanding how to connect to a target over the HTB VPN. The box requires only basic reconnaissance and a telnet connection to gain access.

Enumeration: After confirming the host was up with ping, I ran an Nmap scan (nmap -sV -p- <IP>) which revealed port 23/tcp open, running the Telnet service.

Foothold: I connected via telnet <IP> and attempted a login as root with no password — this succeeded immediately, indicating the box allows unauthenticated root access over Telnet.

Flags: Using ls to enumerate the filesystem, I located and read the flag with cat <path>.

What I Learned: How to verify a host is reachable with ping, perform basic service enumeration with Nmap, and connect via Telnet. This box mainly served to confirm my VPN connection to the HTB network was working correctly.
