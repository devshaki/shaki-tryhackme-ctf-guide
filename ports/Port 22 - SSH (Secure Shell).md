If port **22** is open, SSH is likely running. This means you can try to remotely log into the machine.
```bash
ssh <username>@<IP>
```
to log in to a computer using ssh you will need:

- A **valid username**
    
- A **password**

a password could be brute forced using [[Hydra – Login Bruteforce#shh]] 
🚨remember, most of the times you cant brute force.
only use it when you are said something like "change your weak password" 

you can also log in to a server using ssh with a rsa key
```bash
ssh -i id_rsa <username>@<IP>
```
rsa keys could be encrypted, luckily we can find the password using password cracking tool like
[[John the Ripper – Password Cracker]]