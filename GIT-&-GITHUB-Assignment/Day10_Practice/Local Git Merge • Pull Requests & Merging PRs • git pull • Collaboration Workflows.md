

## Assignment 1 - Local Merge

### Goal

The goal of this task is to understand how a feature branch can be merged into the `main` branch locally using Git.

### 1. Make sure `main` is up to date

First, I checked my current branch and updated the `main` branch.

```bash
git checkout main
git status
git pull origin main
```

### 2. Create a new feature branch

```bash
git checkout -b feature-local-merge
```

This command creates a new branch named `feature-local-merge` and switches to it.

### 3. Create `local-merge.txt`

```bash
touch local-merge.txt
```

Inside the file, I wrote:

```text
Today I learned how a local merge works in Git.
A feature branch can be merged into the main branch using git merge.
The merge happens on our local computer before pushing the changes to GitHub.
Local merge is useful for quick work and personal projects.
```

### 4. Stage and commit the file

```bash
git add .
```

```bash
git commit -m "Add local-merge notes"
```

### 5. Switch back to `main`

```bash
git checkout main
```

### 6. Merge the feature branch

```bash
git merge feature-local-merge
```

The changes from `feature-local-merge` are now merged into the local `main` branch.

### 7. Push the updated main branch

```bash
git push origin main
```

### 8. Check the commit history

```bash
git log --oneline -5
```

**Screenshot:**
*Add screenshot of `git log --oneline -5` after the merge here.*

### Result

The `local-merge.txt` file is now present in the `main` branch on GitHub.

**Screenshot:**
*Add screenshot showing `local-merge.txt` on GitHub `main`.*

---

# Assignment 2 - Pull Request Workflow

### Goal

The goal is to understand how a Pull Request is created, reviewed and merged on GitHub.

### 1. Create a feature branch

```bash
git checkout -b feature-pr-practice
```

### 2. Create `pr-practice.txt`

```bash
touch pr-practice.txt
```

Inside the file, I wrote:

```text
A Pull Request is a request to merge changes from one branch into another.
It is created on GitHub after pushing the feature branch.
Pull Requests are useful because team members can review the code before merging.
They allow discussion, comments and suggestions on the changes.
This makes collaboration safer and more organized.
```

### 3. Stage and commit the file

```bash
git add .
```

```bash
git commit -m "Add PR practice notes"
```

### 4. Push the feature branch

```bash
git push -u origin feature-pr-practice
```

### 5. Create the Pull Request on GitHub

On GitHub, I opened a Pull Request from:

```text
feature-pr-practice → main
```

**PR Title:**

```text
Add PR practice notes
```

**PR Description:**

```text
This Pull Request adds notes about Pull Requests and explains why they are useful for team collaboration and code review.
```

### 6. Merge the Pull Request

I merged the Pull Request on GitHub using the:

**Create a merge commit**

option.

### 7. Delete the feature branch

After merging, I deleted the `feature-pr-practice` branch on GitHub to keep the repository clean.

### 8. Update local main

After the Pull Request was merged, I updated my local `main` branch.

```bash
git checkout main
```

```bash
git pull origin main
```

### 9. Confirm the file

I checked my local repository and confirmed that:

```text
pr-practice.txt
```

is now present on the `main` branch.

**Screenshot:**
*Add screenshot of successful `git pull` here.*

**Screenshot:**
*Add screenshot of the merged Pull Request on GitHub here.*

### Result

The Pull Request was successfully merged into `main`, and `git pull origin main` brought the changes from GitHub to my local computer.

**Merged PR Link:**
*Add the GitHub Pull Request link here.*

---

# Assignment 3 - Compare Both Workflows

### 1. Create `comparison.txt`

```bash
touch comparison.txt
```

I wrote the following answers inside the file:

```text
Local merge happens on our own computer using git merge, while PR merge happens on GitHub.

I would prefer a local merge for personal projects or when I need to quickly merge my own changes.

A Pull Request is better for team projects because other members can review and discuss the changes before merging.

After merging a PR on GitHub, I use git pull origin main to bring the changes to my local main branch.

git pull performs two main steps: git fetch and git merge. It downloads the remote changes and then merges them into the current local branch.
```

### 2. Commit the file

```bash
git add comparison.txt
```

```bash
git commit -m "Add workflow comparison"
```

### 3. Push the changes

```bash
git push origin main
```

### Comparison

| Local Merge                               | Pull Request Merge                            |
| ----------------------------------------- | --------------------------------------------- |
| Happens on my computer.                   | Happens on GitHub.                            |
| Uses `git merge`.                         | Uses the GitHub Pull Request interface.       |
| Usually does not have a review process.   | Allows review and discussion.                 |
| Useful for personal or quick work.        | Better for team collaboration.                |
| Changes are pushed after the local merge. | After merging, local `main` needs `git pull`. |

### Result

I understood that a local merge is faster and happens directly on my computer, while a Pull Request provides a proper review process and is more suitable for team projects.

---

# Assignment 4 - `git pull` Practice

### 1. Switch to main

```bash
git checkout main
```

### 2. Pull the latest changes

```bash
git pull origin main
```

This command checks the remote `main` branch and brings the latest changes to my local `main`.

### 3. Make a small change on GitHub

I edited a file directly using the GitHub web editor and committed the change to the `main` branch.

### 4. Pull the web change to my computer

Back in Git Bash, I ran:

```bash
git pull origin main
```

The new change made on GitHub was downloaded and merged into my local `main` branch.

### 5. Confirm the change

I opened the changed file on my computer and confirmed that the changes made on GitHub were now available locally.

**Screenshot:**
*Add screenshot of the terminal showing the successful `git pull` here.*

### What does `git pull` do?

`git pull` is basically a combination of:

```text
git fetch + git merge
```

`git fetch` downloads the latest changes from the remote repository, and `git merge` combines those changes with the current local branch.

---

# Bonus Assignment - Mini Collaboration Simulation

### 1. Create the first feature branch

```bash
git checkout -b feature-A
```

I added a file, committed it and pushed the branch:

```bash
git add .
git commit -m "Add feature A"
git push -u origin feature-A
```

Then I created a Pull Request on GitHub.

### 2. Create the second feature branch

I created another branch:

```bash
git checkout -b feature-B
```

I added a different file and pushed it:

```bash
git add .
git commit -m "Add feature B"
git push -u origin feature-B
```

Then I created another Pull Request.

### 3. Merge both Pull Requests

I merged both Pull Requests on GitHub one after another.

### 4. Update local main

After both PRs were merged, I ran:

```bash
git checkout main
git pull origin main
```

Both feature files were now available in my local `main` branch.

### 5. What I observed

I observed that after multiple Pull Requests are merged on GitHub, the local `main` branch does not automatically receive those changes. We need to run `git pull` to update the local branch.

---

# Key Takeaways

1. **Local merge** combines branches directly on our computer.
2. **Pull Request merge** happens on GitHub and allows code review and discussion.
3. `git pull` brings remote changes into our current local branch.
4. `git pull` is basically **`git fetch + git merge`**.
5. We should always keep our local `main` updated before starting new work.
