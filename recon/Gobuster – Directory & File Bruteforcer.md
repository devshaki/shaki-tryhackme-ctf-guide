used to find **hidden directories** or **files** on a website.  
only works on [[Port 80 – HTTP (Web Server)]] or **443** (https).

basic usage:
```bash
gobuster dir -u http://<IP> -w /usr/share/wordlists/dirb/common.txt
```
kali recommended wordlists:
- `/usr/share/wordlists/dirb/common.txt` (fast and simple, works most of the times)
- `/usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt` (bigger)

specific usage
```bash
gobuster dir -u http://<IP> -w /usr/share/wordlists/dirb/common.txt -x php,txt,html
```
looks only for .php, .txt and .html files.

## 💡what are we looking for?
	we are looking for any page that we are not supposed to have access,
	for example a admin control panel that is secured badly.

- a [[Upload File Page]] a upload file page could let us gain shell by injecting payloads
- a admin control panel that were not locked
- folders that were left open