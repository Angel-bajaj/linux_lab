# Advanced file linux commands

## 1. File Manipulation Commands
> touch – Create or Update File Timestamps
```
# Create an empty file
touch file1.txt

# Update timestamp of an existing file
touch existing.txt

# Create multiple files at once
touch file2.txt file3.txt

```

## cp – Copy Files and Directories
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

## mv – Move or Rename Files
```
# Rename a file
mv oldname.txt newname.txt

# Move file to another directory
mv file.txt /path/to/destination/

# Move and overwrite without prompt
mv -f file.txt /destination/

```