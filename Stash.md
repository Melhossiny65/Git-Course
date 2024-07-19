In Git, "stash" is a useful feature that allows you to temporarily save changes that are not yet ready to be committed. This is especially handy if you need to switch branches or perform other operations without committing incomplete work. Here’s a quick guide on how to use Git stash:

### Basic Commands

1. **Stash Changes**:
   ```bash
   git stash
   ```
   This command saves your local modifications and reverts the working directory to match the HEAD commit.

2. **List Stashes**:
   ```bash
   git stash list
   ```
   This command lists all stashes that you have saved.

3. **Apply Stash**:
   ```bash
   git stash apply
   ```
   This command applies the most recent stash to your working directory. If you want to apply a specific stash, you can specify it by name:
   ```bash
   git stash apply stash@{2}
   ```

4. **Drop Stash**:
   ```bash
   git stash drop
   ```
   This command removes the most recent stash from the stash list. You can also specify a particular stash to drop:
   ```bash
   git stash drop stash@{2}
   ```

5. **Pop Stash**:
   ```bash
   git stash pop
   ```
   This command applies the most recent stash and then removes it from the stash list. Similar to apply, you can specify a particular stash to pop:
   ```bash
   git stash pop stash@{2}
   ```

6. **Create a Branch from Stash**:
   ```bash
   git stash branch <branchname>
   ```
   This command creates a new branch from the specified stash and then applies the stash to that branch.

### Example Workflow

1. **Stash Changes**:
   ```bash
   git stash
   ```
   Your working directory is now clean, and your changes are saved in a stash.

2. **Switch Branch**:
   ```bash
   git checkout other-branch
   ```
   You can now switch to another branch without worrying about losing your changes.

3. **Apply Stash**:
   ```bash
   git checkout your-branch
   git stash apply
   ```
   After switching back to your original branch, you can apply your saved changes.

4. **Commit Changes**:
   ```bash
   git add .
   git commit -m "Your commit message"
   ```

5. **Drop Stash** (if applied):
   ```bash
   git stash drop
   ```

### Tips

- Use `git stash save "message"` to save a stash with a descriptive message.
- Use `git stash show -p stash@{0}` to view the changes in a specific stash.
- If you need to stash untracked files, use `git stash -u`.

Stashing is a powerful feature that can help manage your work in progress and keep your branches clean.
