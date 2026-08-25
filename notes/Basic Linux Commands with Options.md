# Basic Linux Commands

## 1. `pwd` — Print Working Directory

Shows the absolute path of the current working directory.

### Syntax

```bash
pwd [OPTION]
```

### Common Options

| Option | Description |
|---|---|
| `-L` | Display the logical path, including symbolic links |
| `-P` | Display the physical path without symbolic links |

### Examples

```bash
pwd
```

```bash
pwd -P
```

---

# 2. `ls` — List Directory Contents

Lists files and directories.

### Syntax

```bash
ls [OPTION] [FILE/DIRECTORY]
```

### Common Options

| Option | Description |
|---|---|
| `-l` | Long listing format; shows permissions, owner, size, date, etc. |
| `-a` | Shows all files, including hidden files |
| `-h` | Shows file sizes in human-readable format |
| `-R` | Lists directories recursively |
| `-t` | Sorts files by modification time |
| `-r` | Reverses the sorting order |
| `-S` | Sorts files by size |
| `-d` | Shows information about the directory itself instead of its contents |

### Examples

```bash
ls
```

```bash
ls -l
```

```bash
ls -a
```

```bash
ls -lh
```

```bash
ls -la
```

```bash
ls -ltr
```

```bash
ls -lhS
```

---

# 3. `cd` — Change Directory

Changes the current working directory.

### Syntax

```bash
cd [DIRECTORY]
```

### Common Usage

| Command | Description |
|---|---|
| `cd directory` | Move into a directory |
| `cd ..` | Move to the parent directory |
| `cd ~` | Move to the home directory |
| `cd /` | Move to the root directory |
| `cd -` | Move to the previous directory |
| `cd` | Move to the home directory |

### Examples

```bash
cd projects
```

```bash
cd ..
```

```bash
cd /home/user/projects
```

```bash
cd -
```

> `cd` does not have many commonly used options. Most of its usage is based on different types of paths.

---

# 4. `mkdir` — Make Directory

Creates a new directory.

### Syntax

```bash
mkdir [OPTION] DIRECTORY
```

### Common Options

| Option | Description |
|---|---|
| `-p` | Creates parent directories if they do not exist |
| `-v` | Displays a message for every directory created |
| `-m` | Sets directory permissions while creating it |

### Examples

```bash
mkdir project
```

```bash
mkdir -p project/src/components
```

```bash
mkdir -v project
```

```bash
mkdir -m 755 project
```

---

# 5. `touch` — Create or Update a File

Creates an empty file if the file does not exist.

If the file already exists, it updates its timestamps.

### Syntax

```bash
touch [OPTION] FILE
```

### Common Options

| Option | Description |
|---|---|
| `-a` | Changes only the access time |
| `-m` | Changes only the modification time |
| `-c` | Does not create a file if it does not exist |
| `-t` | Sets a specific timestamp |

### Examples

```bash
touch file.txt
```

```bash
touch file1.txt file2.txt file3.txt
```

```bash
touch -c file.txt
```

---

# 6. `cat` — Display File Contents

Displays the contents of one or more files.

### Syntax

```bash
cat [OPTION] [FILE]
```

### Common Options

| Option | Description |
|---|---|
| `-n` | Shows line numbers for all lines |
| `-b` | Shows line numbers only for non-empty lines |
| `-s` | Removes repeated blank lines |
| `-E` | Shows `$` at the end of each line |
| `-T` | Shows tab characters |

### Examples

```bash
cat file.txt
```

```bash
cat -n file.txt
```

```bash
cat -b file.txt
```

### Combine files

```bash
cat file1.txt file2.txt
```

### Create a file using `cat`

```bash
cat > file.txt
```

Type the content and press:

```text
Ctrl + D
```

---

# 7. `cp` — Copy Files and Directories

Copies files or directories.

### Syntax

```bash
cp [OPTION] SOURCE DESTINATION
```

### Common Options

| Option | Description |
|---|---|
| `-r` | Copies directories recursively |
| `-i` | Asks for confirmation before overwriting |
| `-f` | Forces copying by overwriting the destination |
| `-v` | Shows what is being copied |
| `-u` | Copies only when the source is newer or destination is missing |
| `-p` | Preserves file attributes such as permissions and timestamps |

### Examples

```bash
cp file.txt backup.txt
```

```bash
cp file.txt documents/
```

```bash
cp -r project project_backup
```

```bash
cp -i file.txt backup.txt
```

```bash
cp -rv project project_backup
```

---

# 8. `mv` — Move or Rename

Moves files/directories or renames them.

### Syntax

```bash
mv [OPTION] SOURCE DESTINATION
```

### Common Options

| Option | Description |
|---|---|
| `-i` | Asks before overwriting |
| `-f` | Forces overwrite |
| `-v` | Shows what is being moved |
| `-n` | Does not overwrite an existing file |

### Examples

### Move a file

```bash
mv file.txt documents/
```

### Rename a file

```bash
mv old.txt new.txt
```

### Move a directory

```bash
mv project projects/
```

### Interactive move

```bash
mv -i file.txt documents/
```

---

# 9. `rm` — Remove Files or Directories

Deletes files and directories.

### Syntax

```bash
rm [OPTION] FILE
```

### Common Options

| Option | Description |
|---|---|
| `-i` | Asks for confirmation before deleting |
| `-f` | Forces deletion without confirmation |
| `-r` | Deletes directories recursively |
| `-v` | Shows what is being deleted |

### Examples

### Delete a file

```bash
rm file.txt
```

### Delete multiple files

```bash
rm file1.txt file2.txt
```

### Delete a directory

```bash
rm -r project
```

### Forcefully delete a directory

```bash
rm -rf project
```

### Safer deletion

```bash
rm -i file.txt
```

> **Warning:** `rm` permanently removes files. There is normally no recycle bin.

---

# 10. `echo` — Display Text

Prints text or variable values to the terminal.

### Syntax

```bash
echo [OPTION] [TEXT]
```

### Common Options

| Option | Description |
|---|---|
| `-n` | Does not print a newline at the end |
| `-e` | Enables interpretation of escape characters |

### Examples

```bash
echo "Hello World"
```

```bash
echo -n "Hello"
```

```bash
echo -e "Hello\nWorld"
```

### Write to a file

```bash
echo "Hello World" > file.txt
```

### Append to a file

```bash
echo "New Line" >> file.txt
```

---

# 11. `head` — Display Beginning of a File

Displays the first lines of a file.

### Syntax

```bash
head [OPTION] [FILE]
```

### Common Options

| Option | Description |
|---|---|
| `-n NUMBER` | Displays the first NUMBER lines |
| `-c NUMBER` | Displays the first NUMBER bytes |
| `-q` | Does not display file names when multiple files are used |
| `-v` | Always displays file names |

### Examples

```bash
head file.txt
```

```bash
head -n 5 file.txt
```

```bash
head -c 20 file.txt
```

---

# 12. `tail` — Display End of a File

Displays the last lines of a file.

### Syntax

```bash
tail [OPTION] [FILE]
```

### Common Options

| Option | Description |
|---|---|
| `-n NUMBER` | Displays the last NUMBER lines |
| `-c NUMBER` | Displays the last NUMBER bytes |
| `-f` | Continuously monitors the file |
| `-F` | Similar to `-f`, but continues following if the file is recreated |
| `-q` | Does not display file names |
| `-v` | Always displays file names |

### Examples

```bash
tail file.txt
```

```bash
tail -n 5 file.txt
```

### Monitor logs

```bash
tail -f app.log
```

This is very commonly used when working with application logs.

---

# 13. `less` — Read Large Files

Allows you to view a file page by page.

### Syntax

```bash
less [OPTION] FILE
```

### Common Options

| Option | Description |
|---|---|
| `-N` | Shows line numbers |
| `-S` | Prevents long lines from wrapping |

### Examples

```bash
less file.txt
```

```bash
less -N file.txt
```

### Useful Keys

| Key | Action |
|---|---|
| `Space` | Next page |
| `b` | Previous page |
| `↑` | Move up |
| `↓` | Move down |
| `/word` | Search for a word |
| `n` | Next search result |
| `q` | Quit |

---

# 14. `grep` — Search Text

Searches for a pattern inside files.

### Syntax

```bash
grep [OPTION] PATTERN FILE
```

### Common Options

| Option | Description |
|---|---|
| `-i` | Case-insensitive search |
| `-r` | Search recursively inside directories |
| `-n` | Shows line numbers |
| `-v` | Shows lines that do not match |
| `-c` | Counts matching lines |
| `-l` | Shows only filenames containing the match |
| `-w` | Matches complete words |
| `-E` | Enables extended regular expressions |

### Examples

```bash
grep "error" app.log
```

### Case-insensitive search

```bash
grep -i "error" app.log
```

### Show line numbers

```bash
grep -n "error" app.log
```

### Search recursively

```bash
grep -r "error" .
```

### Count matches

```bash
grep -c "error" app.log
```

---

# 15. `find` — Find Files and Directories

Searches for files and directories.

### Syntax

```bash
find [PATH] [OPTION] [EXPRESSION]
```

### Common Options / Expressions

| Option | Description |
|---|---|
| `-name` | Searches by exact filename pattern |
| `-iname` | Searches by filename without case sensitivity |
| `-type f` | Searches only for files |
| `-type d` | Searches only for directories |
| `-size` | Searches based on file size |
| `-mtime` | Searches based on modification time |
| `-empty` | Finds empty files/directories |

### Examples

### Find a file

```bash
find . -name "test.txt"
```

### Find all Java files

```bash
find . -name "*.java"
```

### Find only directories

```bash
find . -type d
```

### Find only files

```bash
find . -type f
```

### Case-insensitive search

```bash
find . -iname "*.JPG"
```

---

# 16. `wc` — Word Count

Counts lines, words, and bytes/characters.

### Syntax

```bash
wc [OPTION] FILE
```

### Common Options

| Option | Description |
|---|---|
| `-l` | Counts lines |
| `-w` | Counts words |
| `-c` | Counts bytes |
| `-m` | Counts characters |

### Examples

```bash
wc file.txt
```

```bash
wc -l file.txt
```

```bash
wc -w file.txt
```

```bash
wc -c file.txt
```

---

# 17. `sort` — Sort Lines

Sorts lines of text.

### Syntax

```bash
sort [OPTION] FILE
```

### Common Options

| Option | Description |
|---|---|
| `-r` | Reverse order |
| `-n` | Numeric sorting |
| `-f` | Ignore case |
| `-u` | Remove duplicate lines |
| `-k` | Sort based on a specific field |

### Examples

```bash
sort file.txt
```

```bash
sort -r file.txt
```

```bash
sort -n numbers.txt
```

```bash
sort -u file.txt
```

---

# 18. `chmod` — Change File Permissions

Changes permissions of files and directories.

### Syntax

```bash
chmod [OPTION] MODE FILE
```

### Common Options

| Option | Description |
|---|---|
| `-R` | Changes permissions recursively |
| `-v` | Shows a message for every processed file |
| `-c` | Reports only when a change is made |

### Examples

### Add execute permission

```bash
chmod +x script.sh
```

### Remove execute permission

```bash
chmod -x script.sh
```

### Set permissions using numeric notation

```bash
chmod 755 script.sh
```

### Apply recursively

```bash
chmod -R 755 project/
```

---

# 19. `sudo` — Execute as Administrator

Runs a command with elevated privileges.

### Syntax

```bash
sudo command
```

### Examples

```bash
sudo apt update
```

```bash
sudo mkdir /example
```

```bash
sudo systemctl restart nginx
```

> `sudo` may ask for the current user's password.

---

# 20. `whoami` — Show Current User

Displays the username of the current user.

```bash
whoami
```

---

# 21. `history` — Command History

Displays previously executed commands.

### Syntax

```bash
history [OPTION]
```

### Common Usage

```bash
history
```

Show the last 10 commands:

```bash
history 10
```

Search command history:

```text
Ctrl + R
```

---

# 22. `clear` — Clear Terminal

Clears the terminal screen.

```bash
clear
```

Shortcut:

```text
Ctrl + L
```

---

# 23. `date` — Display Date and Time

Displays the current date and time.

```bash
date
```

---

# 24. `file` — Identify File Type

Determines the type of a file.

### Syntax

```bash
file FILE
```

### Example

```bash
file test.txt
```

```bash
file image.png
```

---

# 25. `du` — Disk Usage

Shows how much disk space files and directories are using.

### Common Options

| Option | Description |
|---|---|
| `-h` | Human-readable sizes |
| `-s` | Shows only the total |
| `-a` | Shows all files |

### Examples

```bash
du -h
```

```bash
du -sh project/
```

```bash
du -ah project/
```

---

# 26. `df` — Disk Free Space

Shows available disk space on filesystems.

### Common Options

| Option | Description |
|---|---|
| `-h` | Human-readable format |
| `-T` | Shows filesystem type |
| `-i` | Shows inode usage |

### Examples

```bash
df -h
```

```bash
df -hT
```

---

# 27. `ps` — Process Status

Displays currently running processes.

### Common Options

| Option | Description |
|---|---|
| `-e` | Shows all processes |
| `-f` | Shows detailed information |
| `-u` | Shows processes for a specific user |

### Examples

```bash
ps
```

```bash
ps -ef
```

```bash
ps -u username
```

---

# 28. `kill` — Terminate a Process

Terminates a process using its Process ID (PID).

### Syntax

```bash
kill [OPTION] PID
```

### Common Options

| Option | Description |
|---|---|
| `-15` | Gracefully terminates the process |
| `-9` | Forcefully terminates the process |
| `-2` | Sends interrupt signal |

### Examples

```bash
kill 1234
```

```bash
kill -9 1234
```

> Prefer a normal `kill PID` first. Use `kill -9` only when the process does not terminate normally.

---

# 29. `top` — Monitor Processes

Displays running processes and system resource usage in real time.

```bash
top
```

Press:

```text
q
```

to exit.

---

# 30. `nano` — Terminal Text Editor

Opens a file in the Nano editor.

```bash
nano file.txt
```

Useful shortcuts:

```text
Ctrl + O  → Save
Ctrl + X  → Exit
Ctrl + W  → Search
Ctrl + K  → Cut line
Ctrl + U  → Paste line
```

---

# Linux Path Symbols

| Symbol | Meaning |
|---|---|
| `.` | Current directory |
| `..` | Parent directory |
| `~` | Current user's home directory |
| `/` | Root directory |
| `*` | Wildcard |
| `?` | Matches a single character |

### Examples

```bash
cd ..
```

```bash
cd ~/projects
```

```bash
ls *.java
```

```bash
find . -name "test?.txt"
```

---

# Redirection Operators

## `>`

Redirects output to a file and **overwrites** existing content.

```bash
echo "Hello" > file.txt
```

## `>>`

Redirects output and **appends** to the file.

```bash
echo "New Line" >> file.txt
```

## `<`

Takes input from a file.

```bash
command < file.txt
```

---

# Pipe `|`

Sends the output of one command as the input of another command.

### Syntax

```bash
command1 | command2
```

### Examples

```bash
ls | grep ".java"
```

```bash
ps -ef | grep "node"
```

```bash
cat file.txt | grep "error"
```

---

# Command Combination Examples

### Count Java files

```bash
find . -name "*.java" | wc -l
```

### Find errors in log files

```bash
grep -r "error" . 
```

### Find Java files containing a particular word

```bash
find . -name "*.java" | xargs grep "class"
```

### Show the largest files

```bash
du -ah . | sort -h
```

---

# Most Important Commands for Beginners

```text
pwd       → Current directory
ls        → List files
cd        → Change directory
mkdir     → Create directory
touch     → Create file
cat       → Read file
cp        → Copy
mv        → Move/Rename
rm        → Delete
echo      → Print text
head      → Beginning of file
tail      → End of file
less      → Read file page by page
grep      → Search text
find      → Find files/directories
chmod     → Change permissions
sudo      → Run as administrator
ps        → View processes
kill      → Terminate process
df        → Disk space
du        → Directory/file size
history   → Command history
clear     → Clear terminal
man       → Command manual
```