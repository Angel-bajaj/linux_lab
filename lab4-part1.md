# Advanced file linux commands

## 🚀1. File Manipulation Commands
> touch – Create or Update File Timestamps

```
# Create an empty file
touch file1.txt

# Update timestamp of an existing file
touch existing.txt

# Create multiple files at once
touch file2.txt file3.txt

```

## 🚀cp – Copy Files and Directories

```
# Copy a file
cp source.txt destination.txt

# Copy to another directory
cp source.txt /path/to/destination/

# Copy directory recursively
cp -r dir1 dir2

# Preserve file attributes (timestamps, permissions)
cp -p source.txt backup.txt

```

## 🚀mv – Move or Rename Files

```
# Rename a file
mv oldname.txt newname.txt

# Move file to another directory
mv file.txt /path/to/destination/

# Move and overwrite without prompt
mv -f file.txt /destination/

```
## 🚀rm – Remove Files and Directories
```
# Remove a file
rm file.txt

# Remove multiple files
rm file1.txt file2.txt

# Remove a directory recursively
rm -r foldername/

# Force remove without prompt
rm -rf foldername/
```
## 🚀cat – View or Concatenate Files
```
# Display file contents
cat file.txt

# Combine multiple files into one
cat file1.txt file2.txt > combined.txt

# Display file with line numbers
cat -n file.tx
```

## 🚀less – View File One Page at a Time
```
less file.txt
# Navigation inside less:
# Space → next page
# b → previous page
# q → quit
```
## 🚀head – Show First Lines of a File

```
# First 10 lines (default)
head file.txt

# First 20 lines
head -n 20 file.txt
```

## 🚀tail – Show Last Lines of a File
```
# Last 10 lines (default)
tail file.txt

# Last 15 lines
tail -n 15 file.txt

# Monitor file changes in real-time
tail -f logfile.txt
```

## 🚀2. File Permissions and Ownership
### ✅ls -l – View Detailed File Info
```
ls -l
# Example output:
# -rw-r--r-- 1 user group 1024 Aug 14 10:00 file.txt
# Breakdown:
# [1] -rw-r--r-- → Permissions
# [2] 1 → Hard link count
# [3] user → Owner
# [4] group → Group owner
# [5] 1024 → File size (bytes)
# [6] Aug 14 10:00 → Last modified date/time
# [7] file.txt → File name
```

## 🚀File Permission Structure
- `Owner (u) – File creator`
- `Group (g) – Users in same group`
- `Others (o) – Everyone else Permissions: r (read), w (write), x (execute)`

## 🚀chmod – Change File Permissions
```
# Symbolic method
chmod u+x file.sh   # Add execute for owner
chmod g-w file.txt  # Remove write for group
chmod o+r file.txt  # Add read for others

# Numeric method (r=4, w=2, x=1)
chmod 755 file.sh   # rwxr-xr-x
chmod 644 file.txt  # rw-r--r--
```
## 🚀chown – Change File Owner
```
# Change owner
sudo chown newuser file.txt

# Change owner and group
sudo chown newuser:newgroup file.txt
```

## 🚀chgrp – Change Group
```
sudo chgrp developers file.txt
```
