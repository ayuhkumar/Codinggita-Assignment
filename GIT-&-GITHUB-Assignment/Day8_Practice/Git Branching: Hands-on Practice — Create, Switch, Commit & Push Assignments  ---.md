### Assignment 1: Easy – Understanding Concepts

**Objective:** Check basic understanding of branching.

**Tasks:**
1. What is a **branch** in Git? Explain in your own words.
2. Why should we **not** work directly on the `main` branch?
3. Explain the road analogy of branching (main road vs side road).
4. What is the difference between `git branch` and `git switch`?
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/2b99cc5a-44b5-4a0c-a1b3-6262f88f8341" />



### Assignment 2: Easy – Commands Identification

**Objective:** Identify the correct commands.

**Tasks:**
1. Write the command for the following actions:

| Action                              | Command |
|-------------------------------------|---------|
| List all branches                   |         |
| Create a new branch named `feature-home` |    |
| Switch to `feature-home`            |         |
| Create + Switch in one command      |         |
| Merge `feature-home` into main      |         |
| Delete `feature-home` after merge   |         |

2. Write both the **modern** and **older** command for:
   - Switching to a branch
   - Creating + switching to a new branch


<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/49c047e6-3766-413e-a139-bb0bfcea5ee4" />

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/44e42a20-3729-4a81-b687-1dde3a7794f0" />



### Assignment 3: Medium – Practical Branching Workflow

**Objective:** Perform the complete branching cycle.

**Tasks:**
1. Make sure you are on the `main` branch.
2. Create a new branch named `feature-contact`.
3. Create a file `contact.txt` and write your name + any message.
4. Stage and commit the file with a meaningful message.
5. Switch back to `main`.
6. Merge `feature-contact` into `main`.
7. Delete the `feature-contact` branch.
8. Verify using:
   - `git branch`
   - `git log --oneline`
  


### Assignment 4: Medium – Conceptual + Error Handling

**Objective:** Understand rules and common mistakes.

**Tasks:**
1. What will happen if you try to delete a branch that is not yet merged?  
   Write the error and how to fix it.
2. Why should you always **commit** before switching branches?
3. Fill in the correct flow:

```
______ → Work → ______ → ______ → Switch to main → ______ → Delete branch
```

4. Explain the difference between:
   - `git branch -d branch-name`
   - `git branch -D branch-name`

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/7558ef35-0d82-4000-9971-31405a0ec062" />



### Assignment 5: Difficult – Complete Real Scenario

**Objective:** Apply branching in a realistic situation.

**Scenario:**  
You are working on a website project. Currently you are on the `main` branch. You need to add two new pages: **About** and **Services**.

**Tasks:**
1. Create a branch `feature-about`, add a file `about.txt`, commit it, merge it into `main`, and delete the branch.
2. Create another branch `feature-services`, add a file `services.txt`, commit it, merge it into `main`, and delete the branch.
3. After completing both, show:
   - Final list of branches (`git branch`)
   - Final commit history (`git log --oneline`)
4. Answer:
   - Why did we create two separate branches instead of doing both features on one branch?
   - What is the advantage of merging only after the feature is complete?



<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/26b2f349-1833-457d-bd2e-cb9fd2bd280d" />




