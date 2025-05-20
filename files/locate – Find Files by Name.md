**locate** is used to **quickly search** for files on the system by name.

basic usage:
```bash
locate <filename>
```
**Update the Database:**
	if you're not finding recent files, update the database with:
```bash
	sudo updatedb
```

### 💡shaki pro tip:

- Combine with [[Grep – Search for Text in Files]] for more precise searching:
```bash
locate log | grep apache
```

