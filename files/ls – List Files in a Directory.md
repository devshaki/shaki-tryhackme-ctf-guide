**ls** is used to **view files and directories**.

basic usage:
```bash
ls
```
lists files in the current directory.

Useful Flags:
```bash
ls -l      # long format (shows permissions, owner, size, etc.)
ls -a      # show hidden files (like .bashrc, .git, etc.)
ls -la     # combine both: long + all files
```

### 💡shaki pro tip

after you use ls you can use [[cd – Change Directory]] to get in the folder - ls ../../../.. is unreadable
lets fix it!
```bash
ls ..
cd ..
```