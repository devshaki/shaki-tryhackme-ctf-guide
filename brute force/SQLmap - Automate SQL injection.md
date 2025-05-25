**sqlmap** automates the entire process of exploiting SQL injection vulnerabilities.

❓ what can it do:
- detect if a website is vulnerable to SQL injection vulnerabilities.
- test different types of SQL injection.
- dump entire databases.
- bypass login forms

basic usage: (caveman type shit wtf)
```bash
sqlmap -u "http://example.com/page.php?id=1"
```

pro usage:
	to actually use sqlmap like pro we will get help from [[Burp Suite]] to get us the requests
	from there we can send it to sqlmap to do the magic

1) save the input request using [[Burp Suite]] (for example a login request)
2) should look like this: 
```
POST /login.php HTTP/1.1
Host: example.com
User-Agent: Mozilla/5.0
Cookie: PHPSESSID=abc123
Content-Type: application/x-www-form-urlencoded
Content-Length: 30

username=admin&password=1234
```
3) now we can send it to sqlmap
```bash
sqlmap -r request.txt
```

other flags:
- ```--dbs``` yoinks the database if sqlmap got a successful SQL injection
- ```--threads ```how many threads to run (max 5)
- ```--risk``` tbh no idea just put it on max (max 3)