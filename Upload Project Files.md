To upload your project files from your PC to a new Git repository, follow these steps:

1. **Install Git**: Make sure Git is installed on your PC. You can download it from [git-scm.com](https://git-scm.com/).

2. **Initialize a Local Repository**:
    - Open your terminal or command prompt.
    - Navigate to the directory containing your project files.
    - Initialize a new Git repository with the command:
      ```sh
      git init
      ```

3. **Add Your Files**:
    - Add all your project files to the staging area with:
      ```sh
      git add .
      ```
      This command stages all the files in your project directory.

4. **Commit Your Changes**:
    - Commit the staged files with a descriptive commit message:
      ```sh
      git commit -m "Initial commit"
      ```

5. **Create a New Repository on GitHub**:
    - Go to [GitHub](https://github.com/) and log in.
    - Click the "+" icon in the upper-right corner and select "New repository".
    - Name your repository and configure other options as desired, then click "Create repository".

6. **Add the Remote Repository**:
    - After creating the repository, GitHub will provide you with a URL to use as the remote repository. It will look something like `https://github.com/username/repository.git`.
    - In your terminal, add this remote repository with the command:
      ```sh
      git remote add origin https://github.com/username/repository.git
      ```

7. **Push Your Changes**:
    - Push your local repository to GitHub with:
      ```sh
      git push -u origin master
      ```

Here's a summarized sequence of commands you might use:

```sh
cd /path/to/your/project
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/repository.git
git push -u origin master
```

Replace `/path/to/your/project` with the actual path to your project directory, and `https://github.com/username/repository.git` with the actual URL of your GitHub repository.

This will upload your project files from your PC to the new GitHub repository.
