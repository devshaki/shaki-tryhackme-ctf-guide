used to crack hashed passwords you find on the target

basic usage:
```bash
john hashes.txt
```
🚨**important**
john's default wordlist **SUCKS!!** so i recommended using rockyou most of the times 
```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt
```


John needs the hash in a specific format. There are built-in helper tools like:
```bash
zip2john file.zip > hashes.txt
rar2john file.rar > hashes.txt
pdf2john.pl file.pdf > hashes.txt
7z2john.pl file.7z > hashes.txt
gpg2john file.gpg > hashes.txt
keepass2john file.kdbx > hashes.txt
bcrypt2john file.bcrypt > hashes.txt
office2john.py file.doc > hashes.txt
```
Good luck cracking!