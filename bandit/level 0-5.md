# level 0
## Learned
Connect to a remote machine using SSH
## command used
ssh bandit0@bandit.labs.overthewire.org -p 2220

#level 0->1
## Learned
Using ls to check for files in current directory
using cat to read files
entering a new bandit level by copying the password for it, exitting ssh session and logging in to the next bandit level
rightclick to paste in cmd

## command used
ls
cat readme
ctrl+d(exit), ctrl+v(copy) and rightclick(paste) 

#level 1->2
##learned
Dash - treated specially by commands, often interpreted as a flag or standard input, not a literal filename. 
This ./ means current directory and can be used to read these files that starts with -
##command used
cat ./-

#level 2->3
##learned
1. spaces between words is considered as the argument separator, files with filenames with spaces in it requires quoting,
    " " around it in order to be read
##command used
cat ./"--spaces in this filename--"

#level 3->4
##learned
using ls -a to see hidden files/folders
- -a means all
##command used
ls -a
cat ./...Hiding-From-You

#level 4->5
##learned
using file to see what kind of data is inside the file
using * to run a command on all files in the directory
##command
file ./*
cat ./-file07
