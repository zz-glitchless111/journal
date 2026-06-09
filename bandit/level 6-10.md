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

# Level 5->6
## Learned
## Commands
```bash 
test
```
---

# Level 5->6
## Learned
## Commands
```bash 
test
```
---

# Level 5->6
## Learned
## Commands
```bash 
test
```
---

