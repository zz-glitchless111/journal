# Level 5->6
## Learned
- using `find` command to search for a file with specific attributes
- `.` means current directory, `-type f` means only files, `-size 1033c` means size is 1033 bytes, `! -executable` not executable
## Commands
```bash 
find . -type f -size 1033c ! -executable
cat ./maybehere07/.file2
```
---

# Level 6->7
## Learned
- `/` means absolute directory, the root of all directories
- `-user` to find files belonging to specific users, `-group` to find files belonging to specific groups
- `2>/dev/null` to not display all permission denied returns
 - `2` error output
 - `>` redirect
 - `/dev/null` discards
## Commands
```bash 
find / -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```
password - morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

---

# Level 7->8
## Learned
- `grep` is used to find a word inside a file
## Commands
```bash 
grep "millionth" data.txt
```
password - dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

---

# Level 8->9
## Learned
- `uniq` compares only adjacent duplicate lines, so sorting is required first to group duplicates.
 - `-u` displays only lines that appear exactly once.
 - Since `uniq` only works on adjacent lines, `sort` is used first to group duplicates together.
 - The pipe `|` passes the output of `sort` as input to `uniq`.
## Commands
```bash 
sort data.txt | uniq -u
```
password - 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

---

# Level 9->10
## Learned
- `strings` is used to only extract readable human "strings" from the file
 - `grep` is then used to find the pattern "="
## Commands
```bash 
strings data.txt | grep "="
```
password - FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

---

