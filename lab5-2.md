# 🐚 Shell Tutorial – File Permissions with chmod and chown

## 📌1. Understanding File Permissions in Linux
Each file/directory in linux has :
- `Owner - The user who created the file.`
- `Group - A group of users who may share access.`
- `Others - Everyone else.`

### ✔️ Permission Types
- `r - Read (4 in numeric)`
- `w - Write (2 in numeric)`
- `x - Execute (1 in numeric)`

### ✔️ Permission layouts
Example from ls -l:
```
-rwxr-xr--
```

Breakdown:

- `- → Regular file (d = directory, l = symlink, etc.)`
- `rwx → Owner has read, write, execute`
- `r-x → Group has read, execute`
- `r-- → Others have read only`

## 📌2. chmod – Change File Permissions
#### Syntax
```
chmod [options] mode filename
Modes can be set in numeric (octal) or symbolic form.
```
## (A) Numeric (Octal) Method

Each permission is represented as a number:

- `Read = 4`
- `Write = 2`
- `Execute = 1`
#### Add them up:

- `7 = rwx`
- `6 = rw-`
- `5 = r-x`
- `4 = r--`
- `0 = ---`

#### Example:
chmod 755 script.sh

#### Meaning:

- `Owner: 7 → rwx`
- `Group: 5 → r-x`
- `Others: 5 → r-x`


## (B) Symbolic Method
Use u (user/owner), g (group), o (others), a (all). Operators:

- `+ → Add permission`
- `- → Remove permission`
- `= → Assign exact permission`

#### Examples:
```
chmod u+x script.sh     # Add execute for owner
chmod g-w notes.txt     # Remove write from group
chmod o=r file.txt      # Set others to read only
chmod a+r report.txt    # Everyone gets read access
```