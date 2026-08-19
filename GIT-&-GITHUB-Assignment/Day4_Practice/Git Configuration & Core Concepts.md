# Day 4 - Git Configuration & Core Concepts

## Assignment 1 - Git Configuration

### 1. What is Git Configuration?

Git Configuration is used to set the basic information and preferences that Git uses while working with our projects. It includes details like our username, email and other Git settings.

### 2. Why do we need to configure username and email in Git?

We need to configure our username and email so that Git can identify who made a particular commit. This information is saved with every commit and helps in tracking the changes made by different users.

### 3. Set your Git username

I used the following command to set my Git username:

```bash
git config --global user.name "Your Name"
```

### 4. Set your Git email

I used the following command to set my Git email:

```bash
git config --global user.email "your-email@example.com"
```

### 5. Check the configured username and email

To check my Git username:

```bash
git config --global user.name
```

To check my Git email:

```bash
git config --global user.email
```

### 6. Check all Git configurations

```bash
git config --list
```

This command shows the Git configuration settings available on my system.

---

## Assignment 2 - Git Configuration Levels

### 1. What are the three levels of Git configuration?

Git has three main configuration levels:

1. **System**
2. **Global**
3. **Local**

### 2. Explain System-level configuration.

System-level configuration applies to all users and all repositories on the computer. It is generally used when we want to set a common configuration for the whole system.

```bash
git config --system
```

### 3. Explain Global-level configuration.

Global configuration applies to one particular user and is used for all Git repositories of that user.

For example:

```bash
git config --global user.name "Your Name"
```

### 4. Explain Local-level configuration.

Local configuration applies only to the current Git repository. It can be used when we want different settings for a particular project.

For example:

```bash
git config --local user.name "Your Name"
```

### 5. Difference between Global and Local configuration

| Global Configuration                   | Local Configuration                          |
| -------------------------------------- | -------------------------------------------- |
| Applies to all repositories of a user. | Applies only to one repository.              |
| It is useful for general Git settings. | It is useful for project-specific settings.  |
| Example: global username.              | Example: different username for one project. |

---

## Assignment 3 - Creating a Git Repository

### 1. Create a folder named `Day4_Practice`

```bash
mkdir Day4_Practice
```

### 2. Move inside the folder

```bash
cd Day4_Practice
```

### 3. Initialize the folder as a Git repository

```bash
git init
```

The `git init` command creates a new Git repository in the current folder.

### 4. Check the status of the repository

```bash
git status
```

The `git status` command shows the current state of our Git repository. It tells us about modified, untracked and staged files.

### 5. Check the hidden `.git` folder

```bash
ls -la
```

After using `git init`, a hidden `.git` folder is created inside the project folder.

### 6. What is the `.git` folder?

The `.git` folder contains important information required by Git to manage the repository. It stores the repository's history, configuration and other internal Git data.

We should **not manually delete or modify** this folder because it can damage the Git repository.

---

## Assignment 4 - Git Core Concepts

### 1. What is a Working Directory?

The Working Directory is the folder where we currently work on our project files. When we create or modify files, those changes first appear in the Working Directory.

### 2. What is the Staging Area?

The Staging Area is an intermediate area where we select the changes that we want to include in the next commit.

For example:

```bash
git add file.txt
```

This command moves `file.txt` to the Staging Area.

### 3. What is a Repository?

A Repository is the place where Git stores the history of our project. It contains the commits and other information required to track the changes in the project.

### 4. Explain the basic Git workflow.

The basic Git workflow is:

```text
Working Directory
       ↓
Staging Area
       ↓
Repository
```

First, we create or modify files in the Working Directory. Then we use `git add` to move the required changes to the Staging Area. Finally, we use `git commit` to save those changes permanently in the Git Repository.

### 5. What is a Commit?

A commit is a saved version of our changes in a Git repository. It creates a record of what changes were made at a particular point in time.

Example:

```bash
git commit -m "Added my first file"
```

The message helps us understand what was changed in that commit.

---

## Assignment 5 - Practical Git Commands

### 1. Create a file named `index.html`

```bash
touch index.html
```

### 2. Check the repository status

```bash
git status
```

Since the file is not tracked yet, Git will show `index.html` as an untracked file.

### 3. Add the file to the Staging Area

```bash
git add index.html
```

### 4. Check the status again

```bash
git status
```

Now Git will show `index.html` as a staged file.

### 5. Commit the file

```bash
git commit -m "Added index.html"
```

This saves the staged changes into the Git repository.

### 6. Check the commit history

```bash
git log
```

This command displays the previous commits of the repository.

### 7. View the commit history in a shorter format

```bash
git log --oneline
```

This shows the commits in a shorter and easier-to-read format.

---

## Assignment 6 - Important Git Commands

| Command             | Purpose                                    |
| ------------------- | ------------------------------------------ |
| `git config`        | Used to set and view Git configuration.    |
| `git init`          | Creates a new Git repository.              |
| `git status`        | Shows the current state of the repository. |
| `git add`           | Adds changes to the Staging Area.          |
| `git commit`        | Saves staged changes in the repository.    |
| `git log`           | Shows the commit history.                  |
| `git log --oneline` | Shows a short version of commit history.   |
| `git diff`          | Shows the differences between changes.     |
| `git help`          | Provides help about Git commands.          |

---

## Assignment 7 - Conceptual Questions

### 1. Why is Git configuration important?

Git configuration is important because it provides Git with information about the user and controls how Git behaves. Username and email are especially important because they identify the person who created a commit.

### 2. What happens when we run `git init`?

When we run `git init`, Git creates a new repository in the current directory. It creates a hidden `.git` folder which stores the information needed to manage the repository.

### 3. What is the difference between `git add` and `git commit`?

`git add` moves our selected changes to the Staging Area, while `git commit` saves the staged changes into the Git repository.

In simple words:

```text
git add       → Prepare changes
git commit    → Save changes
```

### 4. Why is the Staging Area useful?

The Staging Area allows us to select which changes should be included in the next commit. This is useful when a project has many changes but we only want to save some of them in a particular commit.

### 5. What happens if we modify a file after committing it?

If we modify a file after committing it, Git detects that the file has changed. The new changes are not automatically part of the previous commit. We need to use `git add` and `git commit` again to save the new changes.

---

## Assignment 8 - Reflection

### Four key takeaways from Day 4

1. I learned how to configure my Git username and email using `git config`.
2. I learned about the **System, Global and Local** configuration levels.
3. I understood the basic Git workflow: **Working Directory → Staging Area → Repository**.
4. I learned how to initialize a repository, stage files, create commits and check commit history.

### What I understood about Git today

Today I understood that Git does not directly save every change as a final version. First, we make changes in the Working Directory, then select them using `git add`, and finally save them using `git commit`. This makes it easier to manage and track the history of a project.
