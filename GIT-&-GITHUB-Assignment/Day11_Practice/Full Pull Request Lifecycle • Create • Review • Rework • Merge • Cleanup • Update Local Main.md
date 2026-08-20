

## Assignment 1 - Complete PR Lifecycle with `feature/contact-form`

### Objective

The goal of this assignment is to practice the complete Pull Request workflow from creating a feature branch to merging it and cleaning up the branches.

### 1. Update the `main` branch

First, I switched to the `main` branch and pulled the latest changes.

```bash
git checkout main
git pull origin main
```

### 2. Create the feature branch

```bash
git checkout -b feature/contact-form
```

This command creates a new branch named `feature/contact-form` and switches to it.

### 3. Create `contact.html`

I created a file named `contact.html` with a simple heading and paragraph.

```html
<h1>Contact Us</h1>
<p>You can use this contact form to get in touch with us.</p>
```

### 4. Stage, commit and push the file

```bash
git add contact.html
git commit -m "Add contact form page"
git push -u origin feature/contact-form
```

### 5. Create the Pull Request

On GitHub, I created a Pull Request with:

**Base branch:** `main`
**Compare branch:** `feature/contact-form`

**PR Title:**

```text
Add contact form page
```

**PR Description:**

```text
This Pull Request adds a simple contact page with a heading and a short description for users who want to contact us.
```

### 6. Merge the Pull Request

I merged the Pull Request using the **Create a merge commit** option.

### 7. Delete the remote branch

After merging the PR, I deleted the remote feature branch.

```bash
git push origin --delete feature/contact-form
```

### 8. Update local `main`

I updated my local `main` using the two-command method.

```bash
git checkout main
git fetch origin main
git merge origin/main
```

`git fetch` downloads the latest information from GitHub, while `git merge` brings those changes into my local `main`.

### 9. Delete the local feature branch

```bash
git branch -d feature/contact-form
```

This safely deletes the local feature branch after its work has already been merged.

### 10. Screenshots

**Screenshot 1:**
*Add screenshot of the merged Pull Request.*

**Screenshot 2:**
*Add screenshot of the terminal after `git fetch` and `git merge`.*

**Screenshot 3:**
*Add screenshot of `git branch` showing that `feature/contact-form` has been deleted.*

**Merged PR Link:**
*Add your GitHub PR link here.*

---

# Assignment 2 - `feature/about-page` with Review & Rework

### Objective

The goal of this assignment is to understand how a developer responds to review comments and updates an existing Pull Request.

### 1. Create the feature branch

```bash
git checkout -b feature/about-page
```

### 2. Create `about.html`

Initially, I created an incomplete `about.html` file with only a heading.

```html
<h1>About Us</h1>
```

### 3. Commit and push the first version

```bash
git add .
git commit -m "Add about page skeleton"
git push -u origin feature/about-page
```

### 4. Create the Pull Request

I created a Pull Request from:

```text
feature/about-page → main
```

**PR Title:**

```text
Add about page
```

**PR Description:**

```text
This Pull Request adds the basic structure of the About page. The page will be improved based on review feedback.
```

### 5. Add a review comment

I added the following review comment to simulate a code review:

```text
Please add a short paragraph about the purpose of the about page and a simple team section placeholder.
```

### 6. Rework the same branch

I made the requested changes in the same `feature/about-page` branch.

The updated file contains:

```html
<h1>About Us</h1>

<p>This page gives information about our project and the people working on it.</p>

<h2>Our Team</h2>
<p>Team members will be listed here.</p>
```

Then I staged, committed and pushed the changes:

```bash
git checkout feature/about-page
git add .
git commit -m "Address review: add description and team section"
git push origin feature/about-page
```

### Why did I use the same branch?

I used the same branch because the existing Pull Request automatically gets updated when new commits are pushed to that branch. There is no need to create another Pull Request.

### 7. Confirm the new commit

After pushing, I checked the Pull Request on GitHub and confirmed that the new commit was visible.

### 8. Merge and clean up

After the review was completed, I merged the Pull Request on GitHub.

Then I deleted the remote branch and updated my local `main`.

```bash
git push origin --delete feature/about-page

git checkout main
git fetch origin main
git merge origin/main

git branch -d feature/about-page
```

### 9. Screenshots

**Screenshot 1:**
*Add screenshot showing the review comment and new rework commit.*

**Screenshot 2:**
*Add screenshot showing the merged Pull Request.*

**PR Link:**
*Add your GitHub PR link here.*

---

# Assignment 3 - `feature/navbar` Independent Full Cycle

### Objective

The goal of this assignment is to independently perform another complete Pull Request lifecycle.

### 1. Create the feature branch

First, I made sure that `main` was updated.

```bash
git checkout main
git pull origin main
```

Then I created the feature branch:

```bash
git checkout -b feature/navbar
```

### 2. Create `navbar.html`

I created `navbar.html` with a heading and information about the navigation bar.

```html
<h1>Navigation Bar</h1>

<p>A navigation bar helps users move between different pages of a website.</p>
<p>It can contain links such as Home, About, Contact and Services.</p>
<p>A good navigation bar makes the website easier to use.</p>
```

### 3. Commit and push

```bash
git add navbar.html
git commit -m "Add navigation bar page"
git push -u origin feature/navbar
```

### 4. Create the Pull Request

I created a Pull Request from:

```text
feature/navbar → main
```

**PR Title:**

```text
Add navigation bar page
```

**PR Description:**

```text
This Pull Request adds a simple page explaining the purpose and common links of a navigation bar.
```

### 5. Merge the Pull Request

After checking the changes, I merged the Pull Request on GitHub.

### 6. Delete the remote branch

```bash
git push origin --delete feature/navbar
```

### 7. Update local `main`

```bash
git checkout main
git fetch origin main
git merge origin/main
```

### 8. Delete the local branch

```bash
git branch -d feature/navbar
```

### 9. Check the commit history

```bash
git log --oneline -10
```

This command shows the latest 10 commits in a short format.

**Screenshot:**
*Add screenshot of `git log --oneline -10` showing the merge commits.*

**Merged PR Link:**
*Add your GitHub PR link here.*

---

# Assignment 4 - Short Reflection

I created a file named `day11-reflection.txt` and wrote the following answers.

### 1. Why do we push new commits to the same feature branch after a review?

We push new commits to the same feature branch because the existing Pull Request is already connected to that branch. When we push new commits to it, the Pull Request automatically gets updated. This keeps the review and all related changes in one place.

### 2. Difference between deleting a remote branch and deleting a local branch

Deleting a **remote branch** removes the branch from GitHub. Deleting a **local branch** removes the branch only from our computer. After a Pull Request is merged, we normally delete both branches to keep the repository clean.

### 3. Why do we run `git fetch` + `git merge` or `git pull` after merging a PR?

When a Pull Request is merged on GitHub, the changes are added to the remote `main` branch. Our local `main` does not automatically receive those changes. Therefore, we use `git fetch` and `git merge`, or simply `git pull`, to update our local `main`.

### 4. Full sequence of commands used to update local `main` and delete the feature branch

```bash
git checkout main
git fetch origin main
git merge origin/main
git branch -d feature/branch-name
```

The `git fetch` command gets the latest remote information, `git merge` updates the local `main`, and `git branch -d` safely deletes the local feature branch.

---

# Overall Learning

From this assignment, I learned the complete Pull Request lifecycle:

```text
Create Feature Branch
        ↓
Create/Edit Files
        ↓
git add
        ↓
git commit
        ↓
git push
        ↓
Create Pull Request
        ↓
Review
        ↓
Rework if Required
        ↓
Push Again to Same Branch
        ↓
Merge Pull Request
        ↓
Delete Remote Branch
        ↓
Update Local main
        ↓
Delete Local Branch
```

### Key Takeaways

1. A feature branch should normally be created from an updated `main`.
2. A Pull Request allows changes to be reviewed before merging.
3. Review changes should be made on the **same feature branch**.
4. After merging a PR, local `main` must be updated using `git fetch` + `git merge` or `git pull`.
5. Feature branches should be deleted after their work is successfully merged.
