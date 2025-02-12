# Managing Branches in Git

To create a new branch, work on it, and then merge it back into the main branch in Git, follow these steps:

### 1. **Create a New Branch**
   First, create a new branch from the main branch (or whichever branch you want to branch off from):
   ```bash
   git checkout main  # Make sure you're on the main branch
   git pull           # Ensure your local main is up-to-date
   git checkout -b new-branch-name  # Create and switch to the new branch
   ```

### 2. **Work on the New Branch**
   Make your changes, edit files, add new files, or delete files as needed. After making changes, stage them and commit:
   ```bash
   git add .  # Stage all changes
   git commit -m "Description of your changes"
   ```

### 3. **Push the New Branch to Remote** (Optional)
   If you're collaborating and want to push your branch to the remote repository:
   ```bash
   git push origin new-branch-name
   ```

### 4. **Switch to the Main Branch**
   Before merging, switch back to the main branch:
   ```bash
   git checkout main
   ```

### 5. **Pull the Latest Changes on Main**
   It’s important to make sure your local `main` is up to date with the remote:
   ```bash
   git pull
   ```

### 6. **Merge Your Feature Branch into Main**
   Merge the changes from the feature branch into the `main` branch:
   ```bash
   git merge new-branch-name
   ```

   If there are conflicts, Git will prompt you to resolve them. After resolving conflicts, commit the changes.

### 7. **Push the Merged Main Branch to Remote**
   Once the merge is complete, push the updated `main` branch to the remote repository:
   ```bash
   git push origin main
   ```

### 8. **Delete the Branch (Optional)**
   After merging, you might want to delete the feature branch both locally and remotely:
   - To delete the local branch:
     ```bash
     git branch -d new-branch-name
     ```
   - To delete the remote branch:
     ```bash
     git push origin --delete new-branch-name
     ```

And that's it! Your feature branch is merged into the main branch. Let me know if you need clarification on any steps!
