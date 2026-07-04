# 🐧 Linux Basics - Day 1

Welcome to my **Linux Learning Journey**!

This repository contains the commands I practiced while learning Ubuntu/Linux. The goal is to understand Linux fundamentals, terminal commands, file management, shell basics, and prepare for Linux/HPC interviews.

---

# 📚 Topics Covered

- Linux Navigation
- User Information
- System Information
- File & Directory Management
- File Editors (Vim & Nano)
- Copying, Moving & Deleting Files
- Viewing File Contents
- Redirection Operators
- Environment Variables
- SSH
- Command History
- Bash Basics

---

# 1. pwd (Print Working Directory)

### Syntax

```bash
pwd
```

### Example

```bash
pwd
```

### Output

```text
/home/gokul/data
```

### Explanation

Displays the complete path of the directory you are currently working in.

---

# 2. uname -a

### Syntax

```bash
uname -a
```

### Example

```bash
uname -a
```

### Output

```text
Linux ubuntu 6.8.0-60-generic x86_64 GNU/Linux
```

### Explanation

Displays complete system information including:

- Kernel Name
- Hostname
- Kernel Version
- Architecture
- Operating System

---

# 3. whoami

### Syntax

```bash
whoami
```

### Output

```text
gokul
```

### Explanation

Displays the username of the currently logged-in user.

---

# 4. clear

### Syntax

```bash
clear
```

### Explanation

Clears the terminal screen.

Shortcut:

```
Ctrl + L
```

---

# 5. history

### Syntax

```bash
history
```

### Output

```text
1 pwd
2 uname -a
3 whoami
...
```

### Explanation

Displays all previously executed commands.

Save history to a file:

```bash
history > history.txt
```

Append history:

```bash
history >> history.txt
```

---

# 6. mkdir

### Syntax

```bash
mkdir folder_name
```

### Example

```bash
mkdir data
```

### Result

```
Creates a new directory called data.
```

---

# 7. cd (Change Directory)

Move into a directory

```bash
cd data
```

Move to Home Directory

```bash
cd
```

or

```bash
cd ~
```

Move one directory back

```bash
cd ..
```

---

# 8. ls (List Files)

### Syntax

```bash
ls
```

### Output

```text
hello.txt
test.txt
```

Useful options

```bash
ls -l
```

Long listing

```bash
ls -a
```

Show hidden files

```bash
ls h*
```

Lists files beginning with **h**

---

# 9. touch

Creates an empty file.

```bash
touch foo.txt
```

Output

```
foo.txt created
```

---

# 10. vim

Open or create a file.

```bash
vim hello.txt
```

Inside Vim

```
i      → Insert mode
Esc    → Exit insert mode
:w     → Save
:q     → Quit
:wq    → Save & Quit
:q!    → Quit without saving
```

---

# 11. nano

Another text editor.

```bash
nano test.txt
```

Save

```
Ctrl + O
```

Exit

```
Ctrl + X
```

---

# 12. cat

Display file contents.

```bash
cat test.txt
```

Output

```text
Hello Linux
Welcome to Ubuntu
```

---

# 13. cp

Copy files.

Syntax

```bash
cp source destination
```

Example

```bash
cp test.txt test1.txt
```

Result

Creates an exact copy.

---

# 14. mv

Move or rename files.

Rename

```bash
mv test1.txt hello.txt
```

Move

```bash
mv hello.txt data/
```

---

# 15. rm

Delete files.

```bash
rm foo.txt
```

Delete folder

```bash
rm -r folder
```

---

# 16. Echo Command

Print text.

```bash
echo "Hello Linux"
```

Output

```text
Hello Linux
```

---

# 17. Output Redirection (>)

Overwrite a file.

```bash
echo "Hello" > file.txt
```

Contents

```
Hello
```

If the file already exists, its old contents are replaced.

---

# 18. Append Redirection (>>)

Append to a file.

```bash
echo "Linux" >> file.txt
```

Contents

```text
Hello
Linux
```

---

# 19. Copy File Contents

```bash
cat hello.txt >> rfile.txt
```

Result

Appends the contents of **hello.txt** to **rfile.txt**.

---

# 20. Absolute Path

```bash
cat /home/gokul/d.txt
```

Starts from the root directory.

---

# 21. Relative Path

```bash
cat d.txt
```

Works only if **d.txt** exists in the current directory.

---

# 22. Home Shortcut (~)

```bash
cat ~/d.txt
```

Equivalent to

```bash
cat /home/gokul/d.txt
```

---

# 23. sudo

Become root user

```bash
sudo -i
```

Install package

```bash
sudo apt-get install vim
```

---

# 24. hostname

```bash
hostname
```

Output

```text
ubuntu
```

Displays system hostname.

---

# 25. SSH

```bash
ssh ubuntu@LAPTOP-971SIGBO
```

Explanation

Connects securely to another Linux machine.

---

# 26. Environment Variables

Correct

```bash
echo $HOME
```

Output

```text
/home/gokul
```

Correct

```bash
echo $USER
```

Output

```text
gokul
```

Wrong

```bash
echo $home
```

Output

```text

```

Explanation

Linux environment variables are **case-sensitive**.

---

# 27. Common Mistakes I Made

❌

```bash
cat data
```

Reason

```
data is a directory.
```

Correct

```bash
ls data
```

or

```bash
cd data
```

---

❌

```bash
echo $home
```

Correct

```bash
echo $HOME
```

---

❌

```bash
echo $user
```

Correct

```bash
echo $USER
```

---

❌

```bash
cat d.
```

Reason

Invalid filename.

---

# Bash Redirection

| Operator | Meaning |
|-----------|----------|
| > | Overwrite |
| >> | Append |
| < | Read input |
| \| | Pipe |

Example

```bash
history > history.txt
```

```bash
echo "Linux" >> file.txt
```

---

# Useful Terminal Shortcuts

| Shortcut | Description |
|------------|------------|
| Ctrl + C | Stop current process |
| Ctrl + L | Clear terminal |
| Ctrl + R | Search history |
| Tab | Auto Complete |
| !! | Repeat previous command |

---

# Commands Practiced Today

- pwd
- uname
- whoami
- clear
- history
- mkdir
- cd
- vim
- nano
- touch
- ls
- cat
- cp
- mv
- rm
- echo
- sudo
- hostname
- ssh

---

# 🎯 What I Learned Today

✅ Linux directory navigation

✅ File creation and deletion

✅ Using Vim & Nano editors

✅ Viewing file contents

✅ Copying and renaming files

✅ Redirection operators (`>` and `>>`)

✅ Absolute vs Relative paths

✅ Environment variables

✅ SSH basics

✅ Command history

---

# 🚀 Next Topics

- chmod
- chown
- grep
- find
- tar
- zip
- Shell Scripting
- Cron Jobs
- Process Management
- Networking Commands
- Bash Variables
