Deleting branches in Git can be done locally or remotely, depending on whether you want to remove a branch from your local repository or from a remote repository. Here’s a step-by-step guide for both scenarios:

### **1. Delete a Local Branch**

To delete a branch locally, follow these steps:

#### **Delete a Local Branch (if not currently checked out)**

1. **List Local Branches:**

   To see a list of all local branches:

   ```sh
   git branch
   ```

2. **Delete the Local Branch:**

   Use the following command to delete a local branch. Replace `branch-name` with the name of the branch you want to delete.

   ```sh
   git branch -d branch-name
   ```

   - **`-d`** (or `--delete`): This option will delete the branch only if it has been fully merged into its upstream branch or another branch. Git will prevent the deletion if there are unmerged changes.

   If you want to forcefully delete a branch even if it has unmerged changes:

   ```sh
   git branch -D branch-name
   ```

   - **`-D`** (or `--delete --force`): This option will delete the branch regardless of its merge status.

#### **Example:**

To delete a branch named `feature` that has been merged:

```sh
git branch -d feature
```

To forcefully delete a branch named `feature` that might have unmerged changes:

```sh
git branch -D feature
```

### **2. Delete a Remote Branch**

To delete a branch from a remote repository, follow these steps:

#### **Delete a Remote Branch**

1. **List Remote Branches:**

   To see a list of all remote branches:

   ```sh
   git branch -r
   ```

2. **Delete the Remote Branch:**

   Use the following command to delete a remote branch. Replace `branch-name` with the name of the branch you want to delete and `remote-name` (usually `origin`) with the name of the remote.

   ```sh
   git push remote-name --delete branch-name
   ```

   **Example:**

   To delete a remote branch named `feature` on the `origin` remote:

   ```sh
   git push origin --delete feature
   ```

   Alternatively, you can also use:

   ```sh
   git push origin :feature
   ```

   Here, the colon `:` syntax indicates that you are deleting the branch `feature` on the remote `origin`.

#### **Clean Up Remote-Tracking Branches**

Sometimes, even after deleting a remote branch, your local repository may still have references to the deleted branch. To clean up these stale references:

```sh
git fetch --prune
```

This command removes references to branches that no longer exist on the remote.

### **Summary**

- **To delete a local branch:**
  - Use `git branch -d branch-name` to delete a merged branch.
  - Use `git branch -D branch-name` to forcefully delete a branch with unmerged changes.

- **To delete a remote branch:**
  - Use `git push remote-name --delete branch-name` or `git push remote-name :branch-name`.

- **To clean up stale remote-tracking branches:**
  - Use `git fetch --prune`.

These commands will help you manage branches effectively and keep your repository organized.
