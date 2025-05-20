**Nmap** is the go-to tool to discover open ports and services running on your target.

basic scan: (never do)
```bash
nmap <IP>
```

detailed scan: (yesir)
```bash
nmap -sC -sV <IP>
```

- `-sC` runs default scripts
- `-sV` detects service versions

by the ports and services you find you can keep diving and finding more info about the target
- [[Port 22 - SSH (Secure Shell)]]
- [[Port 80 – HTTP (Web Server)]]
- [[Port 23 - Telnet]]
- [[Port 21 - FTP (File Transfer Protocol)]]

also by knowing versions of services we could look for exploits using [[Metasploit – Exploitation Framework]]