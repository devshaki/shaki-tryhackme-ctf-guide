If port **21** is open, FTP (File Transfer Protocol) is likely running. This lets you upload/download files to/from the target server.

```bash
ftp <IP>
```
to log in using ftp you will need:

- A **username** (sometimes just `anonymous` works)
- A **password**

🚨remember!
some ftp servers are open and does not require a password to enter
always try connecting with:
- **Username**: anonymous  
- **Password:** anonymous or blank*

if login requires creds, you can try brute forcing with [[Hydra – Login Bruteforce#ftp]]  
🚨only do this if the target hints at weak credentials or default login.