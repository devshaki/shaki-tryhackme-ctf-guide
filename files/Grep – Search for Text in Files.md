**grep** is a powerful tool to search for specific text patterns inside files or command output.

basic usage:
```bash
	grep <word> <file>
```
	searches for `<word>` in the given file.

Examples:
```bash
grep password config.txt
grep -i flag file.txt           # case-insensitive
grep -r admin /var/www/html     # recursive search in folders

```
better usage:
- `-i` = ignore case
- `-r` = recursive (search folders)
- `-n` = show line numbers
- `-v` = inverse (show lines **not** matching)