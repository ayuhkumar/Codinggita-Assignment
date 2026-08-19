# Day 6 - Git Workflow Practice & Troubleshooting

## Assignment 1 - Complete End-to-End Practice Task

### Objective

The main objective of this task is to practice the complete basic Git workflow, starting from creating a file and ending with pushing it to GitHub.

---

### 1. Open or create the Day 5 practice repository

First, I opened my `Day5_Practice` repository in Git Bash.

If the repository is already available on my computer, I used:

```bash
cd Day5_Practice
```

If I need to clone it from GitHub, I can use:

```bash
git clone <repository-url>
```

Then I moved inside the repository:

```bash
cd Day5_Practice
```

---

### 2. Create a file named `practice.txt`

I created the file using the `touch` command:

```bash
touch practice.txt
```

---

### 3. Add the required information inside the file

I opened `practice.txt` and added the following information:

```text
Name: Ayush Kumar

Git Command Learned: git status

git commit saves the changes in the local repository, while git push uploads those committed changes to the remote GitHub repository.
```

### Explanation

I learned that `git commit` and `git push` perform two different tasks. A commit saves the changes locally in Git, whereas push sends those commits to GitHub.

---

### 4. Run the complete Git workflow

#### Step 1 - Check the repository status

```bash
git status
```

This command shows the current condition of the repository. It helps me see that `practice.txt` is an untracked file.

---

#### Step 2 - Add the file to the Staging Area

```bash
git add .
```

The `git add .` command stages all the changes in the current folder.

---

#### Step 3 - Create a commit

```bash
git commit -m "Added practice file"
```

This command creates a new commit containing the staged changes. The changes are now saved in my local Git repository.

---

#### Step 4 - Check the commit history

```bash
git log --oneline
```

This command displays the commit history in a short format.

I should be able to see a commit similar to:

```text
<commit-id> Added practice file
```

---

#### Step 5 - Check the remote repository

```bash
git remote -v
```

This command shows the GitHub repository connected to my local repository.

The output will look similar to:

```text
origin  https://github.com/username/repository.git (fetch)
origin  https://github.com/username/repository.git (push)
```

---

#### Step 6 - Push the commit to GitHub

```bash
git push origin main
```

This command uploads my local commit to the `main` branch of the remote GitHub repository.

If it is the first time pushing the branch, I can also use:

```bash
git push -u origin main
```

---

### 5. Verify the changes on GitHub

After pushing the changes, I opened my GitHub repository and checked the following:

* `practice.txt` is present in the repository.
* The commit message **"Added practice file"** is visible in the commit history.
* The contents of `practice.txt` are available on GitHub.

**Screenshot:**
*Add screenshot of the GitHub repository showing `practice.txt` here.*

**Screenshot:**
*Add screenshot showing the commit message `Added practice file` here.*

---

## Complete Workflow

The complete workflow I followed was:

```text
Create/Edit File
      ↓
git status
      ↓
git add .
      ↓
git commit -m "Added practice file"
      ↓
git log --oneline
      ↓
git remote -v
      ↓
git push origin main
      ↓
GitHub Repository
```

---

## What I Learned

From this practical task, I understood how changes move through Git.

```text
Working Directory
       ↓ git add
Staging Area
       ↓ git commit
Local Repository
       ↓ git push
Remote Repository (GitHub)
```

`git add` prepares the changes, `git commit` saves them locally, and `git push` uploads them to GitHub.

I also understood that **Git configuration and GitHub authentication are different**. Git configuration tells Git who created a commit, while GitHub authentication checks whether the user has permission to access or push to the GitHub repository.

### Key Takeaways

1. `git status` helps me check the current state of my repository.
2. `git add` moves changes to the Staging Area.
3. `git commit` saves changes in the local repository.
4. `git push` uploads the committed changes to GitHub.
5. Git configuration and GitHub authentication are two different things.
