# 🐚 Shell Scripting Tutorial!!

Shell scripting allows you to **automate tasks** in Linux/Unix by writing commands inside a file that the shell executes line by line.

---

## 1. 🔹 What is a Shell Script?

* A **shell** is a command-line interpreter (e.g., `bash`, `zsh`, `sh`).
* A **shell script** is a text file with a series of commands.
* File usually has **`.sh`** extension, though not mandatory.

**Example: `hello.sh`**

```bash
#!/bin/bash
echo "Hello, World!"
```

Run it:

```bash
chmod +x hello.sh   # make it executable
./hello.sh
```

### 📸Output image of the commands :


---

## 2. 🔹 Variables

Variables store data (text, numbers, paths, etc.).

### Defining variables

```bash
name="Angel"
age=18
```

⚠️ No spaces around `=`.

### Accessing variables

```bash
echo "My name is $name and I am $age years old."
```

Output:

```
My name is Angel and I am 18 years old.
```
### 📸output image of the commands : 



### Environment variables

```bash
echo $HOME   # home directory
echo $USER   # current user
echo $PWD    # present working directory
```

---

## 3. 🔹 User Input

Read input from user with `read`.

```bash
#!/bin/bash
echo "Enter your favorite language:"
read lang
echo "You chose $lang"
```
### 📸Output image of the commands :


---

## 4. 🔹 Conditional Statements (if-else)

```bash
#!/bin/bash
num=10

if [ $num -gt 5 ]; then
    echo "Number is greater than 5"
else
    echo "Number is less than or equal to 5"
fi
```

Operators:

* `-eq` (equal)
* `-ne` (not equal)
* `-gt` (greater than)
* `-lt` (less than)
* `-ge` (greater or equal)
* `-le` (less or equal)
### 📸Output image of the commands :


---

## 5. 🔹 Loops

### For loop

```bash
for i in 1 2 3 4 5
do
    echo "Number: $i"
done
```

Or use a range:

```bash
for i in {1..5}
do
    echo "Iteration $i"
done
```

### While loop

```bash
count=1
while [ $count -le 5 ]
do
    echo "Count: $count"
    ((count++))   # increment
done
```

### Until loop

Runs until condition becomes true.

```bash
x=1
until [ $x -gt 5 ]
do
    echo "Value: $x"
    ((x++))
done
```

---

## 6. 🔹 Functions

Encapsulate reusable code.

```bash
greet() {
    echo "Hello, $1"
}

greet Angel
greet World
```

Output:

```
Hello, Angel
Hello, World
```
###  📸Output image of the commands :

---

## 7. 🔹 Command Line Arguments

Access arguments passed to script:

```bash
#!/bin/bash
echo "Script name: $0"
echo "First argument: $1"
echo "Second argument: $2"
echo "All arguments: $@"
echo "Number of arguments: $#"
```

Run:

```bash
./script.sh apple banana
```

Output:

```
Script name: ./script.sh
First argument: apple
Second argument: banana
All arguments: apple banana
Number of arguments: 2
```
### 📸Output image of the commands :

---

## 8. 🔹 Arrays

```bash
fruits=("apple" "banana" "cherry")

echo "First fruit: ${fruits[0]}"

for fruit in "${fruits[@]}"; do
    echo "Fruit: $fruit"
done
```

---

## 9. 🔹 Useful Commands in Scripts

* `date` → show current date/time
* `whoami` → show current user
* `ls` → list files
* `pwd` → print working directory
* `cat` → read file contents

---

## 10. 🔹 A Practical Example

**Backup script (`backup.sh`):**

```bash
#!/bin/bash
# Backup home directory to /tmp

backup_file="/tmp/home_backup_$(date +%Y%m%d%H%M%S).tar.gz"

tar -czf $backup_file $HOME

echo "Backup saved to $backup_file"
```

Run:

```bash
./backup.sh
```

---


## Extra Questions

### 1. What is the purpose of `#!/bin/bash` at the top of a script?

The line `#!/bin/bash` is called a **shebang** (or **hashbang**), and it serves an important role in shell scripting.

### Explanation:
- **`#!/bin/bash`** specifies the path to the **Bash shell** that will be used to interpret and execute the script.
- This allows the system to know which interpreter (in this case, `bash`) to use when running the script, regardless of the user's current shell environment.

### Why it's important:
- It makes the script **portable**. Even if the script is executed in a different environment, it will always use `/bin/bash` as the interpreter.
- Without this line, the script might not run correctly, or it may run with an incorrect interpreter, depending on the environment.

### Example:

```bash
#!/bin/bash
echo "Hello, World!"
```

## 2. How do you make a script executable?

To make a script executable, you need to change its file permissions to allow execution.

### Steps to Make a Script Executable:

1. **Use `chmod` to add execute permissions**:
   ```bash
### chmod +x script_name.sh Run the script:
After making the script executable, you can run it directly:
./script_name.sh

