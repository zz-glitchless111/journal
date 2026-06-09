# Level 10->11
## Learned
- `base64` is used to encode/decode data using base64 encoding scheme
 - `-d` used to decode a base64 encoded data
## Commands
```bash
base64 -d data.txt
```
password - dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

---

# Level 11->12
## Learned
- `tr` is used to replace a character in a file based on a mapping
  - `tr 'A-Z' 'N-ZA-M'` shifts each letter by 13 positions in the alphabet
## Commands
```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
password - 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

---

# Level 12->13
## Learned
- decompressing a repeatedly compressed file.
  - file was compressed using gunzip, bunzip2 and tar
    - gzip to compress files using gzip, gunzip to decompress gzip files
    - bzip2 to compress files using bzip2, bunzip2 to decompress bzip2 files
    - tar -cf to compress files using tar, tar -xf to decompress tar files.
- Always use `file` after every step to determine the next decompression method.
- `~/` means home directory
- `>` directs output into a file
- `xxd` tool to convert binary to hex representation, vice versa
  - `-r` reverse mode, converts hex rep to machine-readable binary
- 
## Commands
```bash
mkdir tmp
cd tmp
cp ~/data.txt .
xdd -r data.txt > compressed
file compressed
mv compressed data.gz
gunzip data.gz
file data
mv data data.bz2
bunzip2 data.bz2
file data
mv data data.gz
gunzip data.gz
file data
tar -xf data
ls
file data5.bin
tar -xf data5.bin
ls 
file data6.bin
tar -xf data6.bin
ls
file data8.bin
mv data8.bin data.gz
gunzip data.gz
cat data
```
password - FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

---

# Level 13->14
## Learned
- using a private key to enter an ssh session
- transferring a file from an ssh session to local machine using `scp`
- `scp` - secure copy
  - `-P` to specify port instead of `-p`
- `ssh -i` - specifies to use a private key instead for login credentials
## Commands
```bash
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```
password - N/A

---

# Level 14->15
## Learned
- finding current ssh session password
- connecting to specific ports using `nc`
- `nc` used to send/receive data on a specific machine to a specific port
## Commands
```bash
cat /etc/bandit_pass/bandit14
nc localhost 30000
```
password - 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

---


