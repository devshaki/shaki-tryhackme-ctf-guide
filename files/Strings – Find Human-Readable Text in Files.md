**strings** is used to pull **readable ASCII text** out of binary files. Super useful for finding:
- hardcoded credentials
- usernames
- URLs or paths
- comments from developers

basic usage:
```bash
strings <file>
```

💡**pro shaki tip**
	use strings with [[Grep – Search for Text in Files]] for best usage
```
	strings <file> | grep password
	strings <file> | grep -i flag
```

