# level 0
## Learned
- Connect to a remote machine using SSH
## command used
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
---
# level 0->1
## Learned
- Using ls to check for files in current directory
- using cat to read files
- entering a new bandit level by copying the password for it, exitting ssh session and logging in to the next bandit level
## Commands
```bash
ls
cat readme 
```

# level 1->2
## Learned
- Dash - is treated specially by many commands, often interpreted as a flag or standard input, not a literal filename. 
- This ./ means current directory and can be used to read these files that starts with -
## Commands
```bash 
cat ./- 
```

# level 2->3
## Learned
- spaces are used as argument separators, filenames with spaces in it requires quoting,
    " " around it in order to be read
## Commands
```bash 
cat ./"--spaces in this filename--" 
```

# level 3->4
## Learned
- using ls -a to see hidden files/folders
- -a means all
## Commands
```bash
ls -a
cat ./...Hiding-From-You 
```

# level 4->5
## Learned
- using file to see what kind of data is inside the file
- using * to run a command on all files in the directory
## Commands
```bash
file ./*
cat ./-file07
```
