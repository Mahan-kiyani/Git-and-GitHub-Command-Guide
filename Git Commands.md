![git](https://brandlogos.net/wp-content/uploads/2021/11/git-logo.png)


# Git Learn Commands

> A practical guide to the most important Git commands, with simple explanations and real-world examples.
>
> The commands are organized step by step to help you understand Git and use it confidently in your projects.

---

## Table of Contents

* [1. Git Init](#1-git-init)
* [2. Git Status](#2-git-status)
* [3. Git Add to Stage](#3-git-add-to-stage)
* [4. Git Remove from Stage](#4-git-remove-from-stage)
* [5. Git Send to Repository](#5-git-send-to-repository)
* [6. Git Log](#6-git-log)
* [7. Git Add and Commit Both](#7-git-add-and-commit-both)
* [8. Git Show](#8-git-show)
* [9. Git Shortcut Create](#9-git-shortcut-create)
* [10. Git Branch Management](#10-git-branch-management)
* [11. Git Branch Deletion](#11-git-branch-deletion)
* [12. Git Branch Rename](#12-git-branch-rename)
* [13. GitLens in VS Code](#13-gitlens-in-vs-code)
* [14. Git Merge](#14-git-merge)
* [15. Git Commit Message Convention](#15-git-commit-message-convention)
* [16. Git Diff](#16-git-diff)
* [17. Gitignore](#17-gitignore)
* [18. Git Checkout](#18-git-checkout)
* [19. Git Restore](#19-git-restore)
* [20. Git clean](#20-git-clean)
* [21. Git reset](#21-git-reset)
* [22. Git revert](#22-git-revert)
* [23. Git status](#23-git-status)
* [24. Git Clone](#24-git-clone)
* [25. Git Remote](#25-git-remote)
* [26. Git Push](#26-git-push)
* [27. Git Pull](#27-git-pull)
* [28. Git Fetch](#28-git-fetch)

---

## 1. Git Init

```bash
git init
```

> \# Initialize a new Git repository in the current directory

---

## 2. Git Status

```bash
git status
```

> \# Show the current state of the working directory and staging area

---

## 3. Git Add to Stage

| Command               | Description                               |
| --------------------- | ----------------------------------------- |
| `git add <file_name>` | # Add a specific file to the staging area |
| `git add .`           | # Add all changes to the staging area     |

---

## 4. Git Remove from Stage

```bash
git rm --cached <file_name>
```

> \# Stop tracking a file in Git without deleting it from the local directory

---

## 5. Git Send to Repository

> **Note:** The git push command is fully explained in tip 26.

```bash
git commit -m "<your_message>"
```

> \# Create a new commit with a message

```bash
git push origin main
```

> \# Push local commits to the main branch on the remote repository

---

## 6. Git Log

| Command                               | Description                                                     |
| ------------------------------------- | --------------------------------------------------------------- |
| `git log`                             | # Show the commit history                                       |
| `git log --oneline`                   | # Show the commit history in a compact one-line format          |
| `git log --oneline --all`             | # Show all commits from all branches                            |
| `git log --stat`                      | # Show the commit history with the files changed in each commit |
| `git log --graph`                     | # Show the commit history as a graph                            |
| `git log --graph --oneline`           | # Show the commit history as a compact graph                    |
| `git log --after='<year-month-day>'`  | # Show commits made after a specific date                       |
| `git log --before='<year-month-day>'` | # Show commits made before a specific date                      |
| `git log --author='<UserName>'`       | # Show commits made by a specific author                        |

---

## 7. Git Add and Commit Both

```bash
git commit -am "<your_message>"
```

> \# Stage and commit all modified and deleted tracked files

---

## 8. Git Show

| Command                | Description                                                                                        |
| ---------------------- | -------------------------------------------------------------------------------------------------- |
| `git show`             | # Show detailed information about the latest commit, including its changes                         |
| `git show <commit_ID>` | # Display detailed information about a specific commit, including its changes, author, and message |
| `git show`             | # Show detailed information about the latest commit, including its changes                         |
| `git show <commit_ID>` | # Display detailed information about a specific commit, including its changes, author, and message |

---

## 9. Git Shortcut Create

### Create Aliases

| Command                                                          | Description                               |
| ---------------------------------------------------------------- | ----------------------------------------- |
| `git config --local alias.<new command name> "current command"`  | # Create a local alias for a Git command  |
| `git config --global alias.<new command name> "current command"` | # Create a global alias for a Git command |

### Show Aliases

| Command                                     | Description                        |
| ------------------------------------------- | ---------------------------------- |
| `git config --local --get-regexp ^alias\.`  | # Show aliases configured locally  |
| `git config --global --get-regexp ^alias\.` | # Show aliases configured globally |

---

## 10. Git Branch Management

### Create and Switch Branches

| Command                       | Description                            |
| ----------------------------- | -------------------------------------- |
| `git branch <branch_name>`    | # Create a new branch                  |
| `git switch <branch_name>`    | # Switch to the specified branch       |
| `git switch -c <branch_name>` | # Create a new branch and switch to it |

### View Branches

| Command         | Description                |
| --------------- | -------------------------- |
| `git branch`    | # Show all local branches  |
| `git branch -r` | # Show all remote branches |

---

## 11. Git Branch Deletion

| Command                       | Description                                                    |
| ----------------------------- | -------------------------------------------------------------- |
| `git branch -d <branch_name>` | # Delete a local branch if it has been fully merged            |
| `git branch -D <branch_name>` | # Force delete a local branch, even if it has unmerged changes |

---

## 12. Git Branch Rename

```bash
git branch -m <new_branch_name>
```

> \# Rename the current branch

---

## 13. GitLens in VS Code

Install the GitLens extension in VS Code to view and manage Git branches with a visual branch graph.

---

## 14. Git Merge

| Command                             | Description                                                                   |
| ----------------------------------- | ----------------------------------------------------------------------------- |
| `git merge <branch_name>`           | # Merge the specified branch into the current branch                          |
| `git merge --no-ff <branch_name>`   | # Merge the specified branch and always create a merge commit                 |
| `git merge --ff-only <branch_name>` | # Merge only if the merge can be completed as a fast-forward                  |
| `git merge --abort`                 | # Abort an unfinished merge and restore the repository to its pre-merge state |

---

## 15. Git Commit Message Convention

### Commit Message Structure

```text
feat: add user authentication

^--^  ^---------------------^
|     |
|     +-> Short description written in the imperative present tense
|
+-------> Type of change
```

### Common Types

| Type        | Description                                                    |
| ----------- | -------------------------------------------------------------- |
| `feat:`     | Add a new feature or functionality                             |
| `fix:`      | Fix a bug or incorrect behavior                                |
| `docs:`     | Add or update documentation                                    |
| `style:`    | Change formatting or code style without changing functionality |
| `refactor:` | Restructure code without changing its behavior                 |
| `test:`     | Add or update tests                                            |
| `chore:`    | Perform maintenance tasks that do not affect the application   |

### Examples

```text
feat: add user authentication

fix: handle invalid email input

docs: update installation instructions

style: format code with black

refactor: simplify user validation

test: add tests for login function

chore: update project dependencies
```

### Commit Message Rules

#### 1. Use a type followed by a colon and a space

```text
feat: add search feature
```

#### 2. Write the description in the imperative present tense

```text
feat: add search feature

fix: handle empty input
```

#### 3. Keep the subject short and clear

```text
feat: add dark mode
```

#### 4. Do not end the subject with a period

```text
Good:  fix: handle invalid input
Bad:   fix: handle invalid input.
```

#### 5. Focus on what the commit does, not how you implemented it

```text
Good:  refactor: simplify user validation
Bad:   refactor: change three if statements to one
```

#### 6. Make each commit focused on one logical change

```text
Good:  feat: add password validation

Avoid: feat: add validation, update docs, and fix login UI
```

---

## 16. Git Diff

| Command                                                | Description                                                             |
| ------------------------------------------------------ | ----------------------------------------------------------------------- |
| `git diff`                                             | # Compare the working directory with the staging area                   |
| `git diff --staged`                                    | # Compare the staging area with the latest commit                       |
| `git diff HEAD`                                        | # Compare the working directory and staging area with the latest commit |
| `git diff <commit_hash>..<commit_hash>`                | # Compare the changes between two commits                               |
| `git diff <commit_hash>..<commit_hash> -- <file_name>` | # Compare a specific file between two commits                           |
| `git diff <branch_name>..<branch_name>`                | # Compare the changes between two branches                              |

---

## 17. Gitignore

[Gitignore Generator](https://www.toptal.com/developers/gitignore/)

> \# Generate a .gitignore file based on your programming language, framework, IDE, and other tools

Create a `.gitignore` file in the root directory of your project.

> \# Tell Git which files and folders should be ignored

### Patterns

| Pattern            | Description                                             |
| ------------------ | ------------------------------------------------------- |
| `*.file_extension` | # Ignore all files with a specific extension            |
| `<file_name>`      | # Ignore a specific file                                |
| `<folder_name>/`   | # Ignore a specific folder                              |
| `<pattern>`        | # Ignore files or folders that match a specific pattern |

### Example

| Pattern          | Description                             |
| ---------------- | --------------------------------------- |
| `*.py`           | # Ignore all Python files               |
| `.env`           | # Ignore the environment variables file |
| `__pycache__/`   | # Ignore the Python cache folder        |
| `<folder_name>/` | # Ignore a specific folder              |

---

## 18. Git Checkout

| Command                                     | Description                                                                      |
| ------------------------------------------- | -------------------------------------------------------------------------------- |
| `git checkout <commit_hash>`                | # Switch to a specific commit                                                    |
| `git checkout <commit_hash> -- <file_name>` | # Restore a specific file from a specific commit                                 |
| `git switch <branch_name>`                  | # Switch to the specified branch                                                 |
| `git log --oneline --all`                   | # Show all commits from all branches                                             |
| `git checkout HEAD~3`                       | # Switch to the commit three steps before HEAD                                   |
| `git checkout HEAD .`                       | # Restore all files in the working directory to their state in the latest commit |

> **Important:** `git checkout` can be used for both commits and branches, but for modern Git, `git switch` is recommended for switching branches and `git restore` for restoring files or discarding changes.

---

## 19. Git Restore

### Restore Working Directory

```bash
git restore <file_name>
```

> \# Discard uncommitted changes in the working directory

```bash
git restore .
```

> \# Discard uncommitted changes in all files in the working directory

### Restore Staging Area

```bash
git restore --staged <file_name>
```

> \# Remove a file from the staging area while keeping its changes in the working directory

```bash
git restore --staged .
```

> \# Remove all files from the staging area while keeping their changes in the working directory

### Restore from a Specific Commit

```bash
git restore --source <commit_hash> <file_name>
```

> \# Restore a file from a specific commit

> *Difference from git checkout: git restore is specifically designed for restoring files and managing working-directory/staging changes, while git checkout has broader uses, including switching branches and commits.*

---

## 20. Git clean

| Command                       | Description                                                           |
| ----------------------------- | --------------------------------------------------------------------- |
| `git clean -h`                | # help for this command                                               |
| `git clean -f -d <file name>` | # Clean working directory by removing all untracked files and folders |

---

## 21. Git reset

| Option    | Command                       | Description                                                                   |
| --------- | ----------------------------- | ----------------------------------------------------------------------------- |
| `--soft`  | `git reset --soft <hash ID>`  | # Reset project to previous commit but keep all changes ready to commit again |
| `--mixed` | `git reset --mixed <hash ID>` | # Reset to previous commit and keep changes unstaged for review               |
| `--hard`  | `git reset --hard <hash ID>`  | # Completely reset project to selected commit (discard all local changes)     |

---

## 22. Git revert

```bash
git revert <hash ID>
```

> \# Revert specific commit by creating a new inverse commit

---

## 23. Git status

| Command         | Description                                                  |
| --------------- | ------------------------------------------------------------ |
| `git status -h` | # Status Help                                                |
| `git status -s` | # Show concise summary of file changes and repository status |

---

## 24. Git Clone

```bash
git clone <repository_url ---> https or ssh>
```

> \# Create a local copy of a remote repository, so you can work on it

---

## 25. Git Remote

| Command                                                  | Description                                                                              |
| -------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `git remote`                                             | # list remote names                                                                      |
| `git remote -v`                                          | # List all remote repositories with their URLs                                           |
| `git remote remove <name>`                               | # Delete a remote repository link from your local repository, so Git no longer tracks it |
| `git remote add <name(origin usually)> <repository_url>` | # Add a new remote repository to your local repository                                   |

---

## 26. Git Push

| Command                                   | Description                                                                                                             |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `git push`                                | # Push the current branch to its default remote repository                                                              |
| `git push <remote_name> <branch_name>`    | # Upload local commits to a remote repository                                                                           |
| `git push -u <remote_name> <branch_name>` | # Push the specified branch to the remote repository and set it as the default branch for future push and pull commands |

---

## 27. Git Pull

```bash
git pull <remote_name> <branch_name>
```

> \# Fetch changes from the remote repository and merge them into the current branch

---

## 28. Git Fetch

```bash
git fetch
```

> \# Download updates from all configured remote repositories without changing your working directory

```bash
git fetch <remote_name>
```

> \# Download updates from a specific remote repository

```bash
git fetch <remote_name> <branch_name>
```

> \# Download updates from a specific remote branch

```bash
git fetch --all
```

> \# Download updates from all configured remote repositories

```bash
git fetch --prune
```

> \# Remove remote-tracking references that no longer exist on the remote

```text
{ git pull == git fetch && git merge }
```
