# Day 3 - CLI, GUI & Essential Git Bash Commands

## Assignment 1: CLI vs GUI

### 1. What is GUI?

GUI stands for **Graphical User Interface**. It allows us to interact with a computer using graphical elements like icons, buttons, windows and the mouse.

### 2. What is CLI?

CLI stands for **Command Line Interface**. It allows us to interact with the computer by typing commands in a terminal.

### 3. Comparison between CLI and GUI

| CLI                                        | GUI                                            |
| ------------------------------------------ | ---------------------------------------------- |
| We use commands by typing them.            | We use icons, buttons and menus.               |
| It is fast for repetitive tasks.           | It is easy to use for beginners.               |
| It is useful for automation and scripting. | It is more visual and user-friendly.           |
| It is commonly used by developers.         | It is commonly used for normal computer tasks. |
| Example: Git Bash                          | Example: Windows File Explorer                 |

### 4. Why do we prefer CLI (Git Bash) for using Git instead of a GUI tool?

We prefer CLI because it gives us more control over Git commands and features. It is also faster after learning the commands and is useful for automation and professional development. Git was originally designed to work through the command line.

### 5. Give 2 examples of GUI and 2 examples of CLI.

**GUI:**

1. Windows File Explorer
2. VS Code

**CLI:**

1. Git Bash
2. Command Prompt (CMD)

---

## Assignment 2: Git Installation & VS Code Setup

### 1. Check Git version

I opened Git Bash and used the following command:

```bash
git --version
```

**Output:**

```text
git version <write the version shown on your computer>
```

For example:

```text
git version 2.43.0
```

### 2. Why do we change the default terminal in VS Code from PowerShell to Git Bash?

We change the terminal to Git Bash because it is convenient for practicing Git commands. It provides a Unix-like command environment and makes it easier to use the Git Bash commands taught in this topic.

### 3. Steps to change the default terminal to Git Bash

1. Open **VS Code**.
2. Press `Ctrl + ,` to open Settings.
3. Search for `terminal default profile windows`.
4. Select **Git Bash** from the dropdown.
5. Open a new terminal using `Ctrl + ``.
6. Now the VS Code terminal will open with Git Bash.

### 4. Screenshots

**Screenshot 1:**
*Add screenshot of Git Bash showing the `git --version` output.*

**Screenshot 2:**
*Add screenshot of VS Code showing Git Bash selected as the terminal.*

---

## Assignment 3: Navigation & Listing Commands

### 1. Commands used in Git Bash

#### Check my current location

```bash
pwd
```

#### Go to home directory

```bash
cd ~
```

#### Create the `Day3_Practice` folder

```bash
mkdir Day3_Practice
```

#### Move into the folder

```bash
cd Day3_Practice
```

#### Create two files

```bash
touch file1.txt file2.txt
```

#### List all files

```bash
ls
```

#### List all files including hidden files in long format

```bash
ls -la
```

#### Move one level up

```bash
cd ..
```

#### Come back into `Day3_Practice`

```bash
cd Day3_Practice
```

### 2. Purpose of the commands

| Command  | Purpose                                                      |
| -------- | ------------------------------------------------------------ |
| `pwd`    | Shows the current working directory.                         |
| `cd ~`   | Takes us to the home directory.                              |
| `cd ..`  | Moves one level up from the current directory.               |
| `cd -`   | Takes us back to the previous directory.                     |
| `ls -la` | Shows all files, including hidden files, in detailed format. |

---

## Assignment 4: File & Folder Operations

### Commands used in Git Bash

### 1. Create a folder named `Project`

```bash
mkdir Project
```

### 2. Move inside the `Project` folder

```bash
cd Project
```

### 3. Create `index.html`

```bash
touch index.html
```

### 4. Create `about.txt` using echo

```bash
echo "This is my project." > about.txt
```

### 5. Copy `index.html` as `home.html`

```bash
cp index.html home.html
```

### 6. Rename `about.txt` to `about-me.txt`

```bash
mv about.txt about-me.txt
```

### 7. Go back and create the `Backup` folder

```bash
cd ..
mkdir Backup
```

### 8. Copy the entire `Project` folder into `Backup`

```bash
cp -r Project Backup/
```

### 9. Delete `home.html`

```bash
cd Project
rm home.html
```

### 10. Show the content of `about-me.txt`

```bash
cat about-me.txt
```

### 11. Delete the `Backup` folder

```bash
cd ..
rm -r Backup
```

### Difference between `rm` and `rm -r`

`rm` is normally used to delete a file, while `rm -r` is used to delete a folder along with the files and folders inside it.

### Why should we be careful while using `rm -rf`?

We should be very careful with `rm -rf` because it forcefully and permanently deletes the specified files or folders. There is usually no normal recycle-bin recovery, so using it on the wrong location can cause loss of important data.

---

## Assignment 5: Command Meaning + Reflection

### 1. Match the commands with their purpose

| Command   | Purpose                                                |
| --------- | ------------------------------------------------------ |
| `pwd`     | Shows the current working directory.                   |
| `ls -la`  | Shows all files including hidden files in long format. |
| `mkdir`   | Creates a new folder.                                  |
| `touch`   | Creates a new empty file.                              |
| `cat`     | Shows the content of a file.                           |
| `mv`      | Moves or renames a file or folder.                     |
| `rm -r`   | Deletes a folder and its contents.                     |
| `clear`   | Clears the terminal screen.                            |
| `whoami`  | Shows the current username.                            |
| `history` | Shows previously used commands.                        |

### 2. Correct commands

**Create an empty file:**

```bash
touch file.txt
```

**Show current date and time:**

```bash
date
```

**Clear the terminal screen:**

```bash
clear
```

**Show previously used commands:**

```bash
history
```

**Go back to the previous directory:**

```bash
cd -
```

### 3. Four key takeaways from Day 3

1. I learned the basic difference between **CLI and GUI** and when they are useful.
2. I learned how to use **Git Bash** and change the VS Code terminal to Git Bash.
3. I learned important commands like `pwd`, `cd`, `ls`, `mkdir` and `touch` for navigation and file management.
4. I learned how to create, copy, rename and delete files and folders using Git Bash commands.
