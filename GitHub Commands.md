Here are the main commands for Git, along with some essential GitHub commands that are used via Git or the GitHub web interface:

### Git Commands

1. **Repository Initialization and Cloning**
   - `git init`: Initialize a new Git repository.
   - `git clone <repository-url>`: Clone an existing repository from a remote server.

2. **Stage and Commit**
   - `git add <file>`: Stage a file for the next commit.
   - `git add .`: Stage all changes in the current directory.
   - `git commit -m "commit message"`: Commit the staged changes with a message.
   - `git commit -a -m "commit message"`: Stage and commit all changes in tracked files with a message.

3. **Branching and Merging**
   - `git branch`: List all branches.
   - `git branch <branch-name>`: Create a new branch.
   - `git checkout <branch-name>`: Switch to a different branch.
   - `git checkout -b <branch-name>`: Create and switch to a new branch.
   - `git merge <branch-name>`: Merge a branch into the current branch.

4. **Pushing and Pulling**
   - `git push`: Push local changes to the remote repository.
   - `git push origin <branch-name>`: Push a specific branch to the remote repository.
   - `git pull`: Fetch and merge changes from the remote repository to the current branch.

5. **Status and Logs**
   - `git status`: Show the status of changes as untracked, modified, or staged.
   - `git log`: Show the commit history.
   - `git log --oneline`: Show the commit history in a compact form.

6. **Remote Repositories**
   - `git remote`: List remote repositories.
   - `git remote add <name> <url>`: Add a new remote repository.
   - `git remote remove <name>`: Remove a remote repository.

7. **Stashing**
   - `git stash`: Stash the current changes.
   - `git stash pop`: Apply the stashed changes.
   - `git stash list`: List all stashes.

8. **Tags**
   - `git tag <tag-name>`: Create a new tag.
   - `git push origin <tag-name>`: Push a tag to the remote repository.

9. **Other Useful Commands**
   - `git diff`: Show changes between commits, commit and working tree, etc.
   - `git reset --hard <commit>`: Reset the working directory and index to a specified commit.
   - `git rm <file>`: Remove a file from the working directory and staging area.

### GitHub Commands and Actions

1. **Forking and Pull Requests**
   - **Fork**: Use the "Fork" button on GitHub to create a personal copy of a repository.
   - **Pull Request (PR)**: Use the "New Pull Request" button on GitHub to propose changes from your branch or fork to the original repository.

2. **Issues and Projects**
   - **Issues**: Use the "Issues" tab to create and manage issues.
   - **Projects**: Use the "Projects" tab to create and manage project boards.

3. **GitHub Actions**
   - **Workflows**: Use the `.github/workflows` directory to define automated workflows.
   - **Triggers**: Define events that trigger workflows (e.g., push, pull_request).

4. **Collaborating**
   - **Add Collaborators**: Use the "Settings" tab of a repository to add collaborators.
   - **Manage Access**: Use the "Manage Access" section under "Settings" to control access levels.

These commands cover the essentials of working with Git and GitHub, enabling you to perform common tasks efficiently.
