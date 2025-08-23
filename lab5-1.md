# What is a shell script?
- `A shell script is a text file containing a series of commands written for the shell to execute.`
- `It automates tasks that you would normally run in the terminal.`
- `Example: Running multiple commands, looping through files, making backups, etc.`
## 2. Creating Your First Shell Script
```
1.Open a terminal and create a file:

nano hello.sh
Add the following content:

#!/bin/bash
# This is a simple shell script

echo "Hello, World!"
#!/bin/bash → called a shebang, tells the system which shell to use.
echo → prints text to the screen.
# → marks a comment.
Save and exit (CTRL+O, CTRL+X in nano).

Make it executable:

chmod +x hello.sh
Run it:

./hello.sh
✅ Output should be:

Hello, World!
