# 🌍Navigation commands

> pwd – Print Working Directory
```
Shows the current location in the filesystem.

📌 Output example:

/Users/yourname/projects
```

## ls – List Directory Contents
Lists files and folders in the current directory.


- `ls -l → Detailed list (permissions, size, date)`
- `ls -a → Shows hidden files (those starting with .)`
- `ls -la → Combined`

cd – Change Directory
Moves into a directory.

cd folder_name
Examples:

cd Documents        # Go to Documents
cd ..               # Go up one level
cd /                # Go to root
cd ~                # Go to home directory
## 📁2. File and Directory Management
```
mkdir – Make Directory
Creates a new folder.

mkdir new_folder
touch – Create File
Creates an empty file.

touch file.txt
cp – Copy Files or Directories
cp source.txt destination.txt
Copy folder:
cp -r folder1 folder2
mv – Move or Rename Files
mv oldname.txt newname.txt
mv file.txt ~/Documents/     # Move file
rm – Remove Files
rm file.txt          # Delete file
rm -r folder_name    # Delete folder (recursively)
⚠️ Be careful! There is no undo.
```
## 📸3. File Viewing & Editing
```
cat – View File Contents
Displays content in terminal.

cat file.txt
nano – Edit Files in Terminal
A basic terminal-based text editor.

nano file.txt
Use arrows to move
CTRL + O to save
CTRL + X to exit
clear – Clears the Terminal
clear
Shortcut: CTRL + L
 
```
## 💬4. System Commands
```
echo – Print Text
Useful for debugging or scripting.

echo "Hello, World!"
whoami – Show Current User
whoami
man – Manual for Any Command
man ls
Use q to quit the manual.
```

## 🔍5. Searching and Finding
```
find – Locate Files
find . -name "*.txt"
🔍 Finds all .txt files in current folder and subfolders.

grep – Search Inside Files
grep "hello" file.txt
🔍 Searches for the word hello inside file.txt.
```
