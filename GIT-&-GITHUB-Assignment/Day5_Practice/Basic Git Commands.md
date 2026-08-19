# Day 5 - Practical Basic Git Commands

## Assignment 1 - Create a Git Repository

### 1. Create a folder named `Day5_Practice`

```bash
mkdir Day5_Practice
```

### 2. Move inside the folder

```bash
cd Day5_Practice
```

### 3. Initialize the folder as a Git repository

```bash
git init
```

The `git init` command initializes the current folder as a Git repository. After running it, Git creates a hidden `.git` folder.

### 4. Check the status of the repository

```bash
git status
```

The `git status` command shows the current state of the repository and tells us about untracked, modified and staged files.

---

## Assignment 2 - Add and Commit Files

### 1. Create a file named `index.html`

```bash
touch index.html
```

### 2. Check the status

```bash
git status
```

The file will appear as an **untracked file** because Git has not started tracking it yet.

### 3. Add the file to the Staging Area

```bash
git add index.html
```

The `git add` command moves the selected file from the Working Directory to the Staging Area.

### 4. Check the status again

```bash
git status
```

Now `index.html` will be shown as a staged file.

### 5. Commit the file

```bash
git commit -m "Added index.html"
```

The `git commit` command saves the staged changes into the Git repository.

---

## Assignment 3 - Working with Multiple Files

### 1. Create three files

```bash
touch home.html about.html contact.html
```

### 2. Check the status

```bash
git status
```

Git will show the three files as untracked files.

### 3. Add all three files to the Staging Area

```bash
git add home.html about.html contact.html
```

### 4. Commit the files

```bash
git commit -m "Added website pages"
```

This creates a new commit containing the three HTML files.

### 5. Add all changes at once

We can also use:

```bash
git add .
```

The `git add .` command stages all the changes in the current directory and its subdirectories.

---

## Assignment 4 - Making and Checking Changes

### 1. Modify `index.html`

I added some content to the `index.html` file.

For example:

```html
<h1>My First Git Project</h1>
```

### 2. Check the status

```bash
git status
```

Git will show that `index.html` has been modified.

### 3. Check what has changed

```bash
git diff
```

The `git diff` command shows the changes made to the files since the last commit.

### 4. Stage the modified file

```bash
git add index.html
```

### 5. Commit the changes

```bash
git commit -m "Updated index page"
```

Now the changes are saved as a new commit.

---

## Assignment 5 - Git Log

### 1. View the complete commit history

```bash
git log
```

The `git log` command displays the commit history of the repository.

It normally shows information such as:

* Commit ID
* Author
* Date
* Commit message

### 2. View a short commit history

```bash
git log --oneline
```

This command shows each commit in a short one-line format, which makes the history easier to read.

### 3. Why is Git history useful?

Git history is useful because it allows us to see the changes made to a project over time. It also helps us understand who made a change and when it was made.

---

## Assignment 6 - Unstage a File

### 1. Create a new file

```bash
touch test.txt
```

### 2. Stage the file

```bash
git add test.txt
```

### 3. Remove the file from the Staging Area

```bash
git restore --staged test.txt
```

This command removes `test.txt` from the Staging Area but does not delete the actual file.

### 4. Check the status

```bash
git status
```

Now `test.txt` will appear as an untracked file again.

---

## Assignment 7 - Basic Git Commands

| Command                | Purpose                                     |
| ---------------------- | ------------------------------------------- |
| `git init`             | Creates a new Git repository.               |
| `git status`           | Shows the current status of the repository. |
| `git add`              | Adds changes to the Staging Area.           |
| `git add .`            | Adds all changes to the Staging Area.       |
| `git commit`           | Saves staged changes in the repository.     |
| `git log`              | Shows the complete commit history.          |
| `git log --oneline`    | Shows a short commit history.               |
| `git diff`             | Shows changes that have not been staged.    |
| `git restore --staged` | Removes a file from the Staging Area.       |

---

## Assignment 8 - Understand the Git Workflow

The basic Git workflow is:

```text
Working Directory
        ↓
    git add
        ↓
Staging Area
        ↓
   git commit
        ↓
   Repository
```

First, we create or modify files in the **Working Directory**. Then we use `git add` to select the changes that we want to save. Finally, `git commit` stores those changes permanently in the Git Repository.

---

## Assignment 9 - Practical Questions

### 1. What is the difference between `git add` and `git commit`?

`git add` moves the changes to the Staging Area, while `git commit` saves the staged changes into the repository.

In simple words:

```text
git add     → Select changes
git commit  → Save changes
```

### 2. What is the difference between `git status` and `git log`?

`git status` shows the current state of our working repository, such as untracked or modified files. `git log` shows the previous commits and the history of the project.

### 3. Why should we write meaningful commit messages?

Meaningful commit messages help us understand what was changed in each commit. They make the project history easier to read and are especially useful when working in a team.

For example:

```bash
git commit -m "Added login page"
```

is better than:

```bash
git commit -m "changes"
```

### 4. Can we commit without using `git add`?

Normally, we first use `git add` to put the changes into the Staging Area and then use `git commit`. This gives us control over which changes should be included in the commit.

---

## Assignment 10 - Reflection

### Four key takeaways from Day 5

1. I learned how to create and initialize a Git repository using `git init`.
2. I learned how to use `git add` and `git commit` to save my project changes.
3. I understood how `git status`, `git diff` and `git log` help us check our project and its history.
4. I learned that the Staging Area gives us control over which changes we want to include in a commit.

### What I understood about Git today

Today I understood how Git is practically used to manage a project. I learned that after making changes, we can check them using `git status` and `git diff`, stage them using `git add`, and finally save them using `git commit`. This makes it easier to maintain the history of our project.
