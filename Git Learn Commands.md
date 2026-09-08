# Git Learn Commands 

1- git init

2- git status

3- Git add to stage
    
    [path] git add 'file name' \#<selected file to stage>
    [path] git add . \#<all file to stage>

4-Git removed stage
    
    [path] git rm --cached 'file name' \# Stop tracking a file in Git without deleting it from the local directory
    
5-Git send to repo (The git push command is fully explained in tip 26)
    
    [path] git commit -m 'your_message'
    git push origin main
    
6-Git Log

    git log
    git log --oneline
    git log --oneline --all \# show all commits 
    git log --stat
    git log --graph
    git log --graph --oneline
    git log --after='year-month-day'
    git log --before='year-month-day'
    git log --authorr='UserName'
    
7-Git Add and Commit both

    git commit -am "file name"

8- Git Show 

    git show \# last changes in project
    git show 'commit_ID' \# Display detailed information about a specific commit, including its changes, author, and message
    
9-Git shortcut create

    git config --local alias.lgo "log --oneline"
    git config --global alias.am "commit -am"
    
    git config --local --get-regexp ^alias\. \#see alias was created in local
    git config --global --get-regexp ^alias\. \#see alias was created in global

-------------------------------------------------------------------------------------------------------------------------------------------------------

10-Git Branch

    git branch \# show branchs on your project
    git branch <branch_name>  \# create a branch
    git branch -r \# List all remote branches available in the connected repositories(use for git fetch and ...)
    git switch <branch_name> \# go to the branch you wish
    git switch -c <branch_name> \# create and go to the branch 
    
11-Git remove a branch
    
    git branch -d <branch name> \# if you on that task you cant delete it, you must be switch
    git branch -D <branch name> \# if you’ve committed or added changes but haven’t merged them into the branch, you need to use -D to delete it.
    
    
12-Git rename branch

    git branch -m <new branch name> \# First, switch to the branch you want, then run this command.
    
13-install gitlens on VsCode and see branch graph on thay

14-Git Merge 
    
    git merge <name of branch> \# First, switch to the branch you want, then run this command. <fast forward>
    git merge <name of branch> <name_commit> \# First, switch to the branch you want, then run this command. <non-fast forward>
    git merge --abort \# Abort unfinished merge and restore repository to pre-merge state


15-Commit Message Semantic
    
    feat: add hat wobble
    ^--^  ^------------^
    |     |
    |     +-> Summary in present tense.
    |
    +-------> Type: chore, docs, feat, fix, refactor, style, or test.
    
    More Examples:

    feat: (new feature for the user, not a new feature for build script)
    fix: (bug fix for the user, not a fix to a build script)
    docs: (changes to the documentation)
    style: (formatting, missing semi colons, etc; no production code change)
    refactor: (refactoring production code, eg. renaming a variable)
    test: (adding missing tests, refactoring tests; no production code change)
    chore: (updating grunt tasks etc; no production code change)

16-Git Comparison

    git diff \# comparison work directory with staging area
    git diff --staged \# comparison stage area with last commits
    git diff <HEAD or head> \# comparison work directory with last commits
    git diff <commit hash code>..<commit hash code> \# comparison one commit to another with hash code (first git log)
    git diff <commit hash code>..<commit hash code> <file name> \# comparison one file in commit to another with hash code (first git log)
    git diff <branch name>..<branch name> \# comparison two branches

17-Gitignore 
    
    create gitignore file '.gitignore' in the path \# https://www.toptal.com/developers/gitignore
    *.file_name \# all files with this suffix is ignore

18-Git checkout

    git checkout <hash name> \# Switch to specific commit
    git switch <master or main>
    git log --oneline --all \# show all commits 
    git checkout <hash name> <file name>
    git checkout HEAD~3 \# Checkout commit three steps before HEAD 

    ** we can use <git checkout Head> Revert working directory to clean state (discard uncommitted changes)

19-Git Restore

    git restore <file name> \# Revert working directory to clean state (discard uncommitted changes)
    git restore --staged <file name> \# Remove files from staging area
    git restore --source <hash name> <file name> \# Restore file(s) from a specific commit as source

20-Git clean

    git clean -h \# help for this command
    git clean -f -d <file name> \# Clean working directory by removing all untracked files and folders

21-Git reset

    git reset --soft <hash ID> \# Reset project to previous commit but keep all changes ready to commit again
    git reset --mixed <hash ID> \# Reset to previous commit and keep changes unstaged for review
    git reset --hard <hash ID> \# Completely reset project to selected commit (discard all local changes)

22-Git revert

    git revert <hash ID> \# Revert specific commit by creating a new inverse commit

23-Git status

    git status -h
    git status -s \# Show concise summary of file changes and repository status

-------------------------------------------------------------------------------------------------------------------------------------------------------

24-Git Clone

    git clone <repository_url ---> https or ssh> \# Create a local copy of a remote repository, so you can work on it

25-Git Remote

    git remote \# list remote names
    git remote -v \# List all remote repositories with their URLs
    git remote remove <name> \# Delete a remote repository link from your local repository, so Git no longer tracks it
    git remote add <name(origin usually)> <repository_url> \# Add a new remote repository to your local repository

26-Git Push

    git push \# Push the current branch to its default remote repository 
    git push <remote_name> <branch_name> \# Upload local commits to a remote repository
    git push -u <remote_name> <branch_name> \# Push the specified branch to the remote repository and set it as the default branch for future push and pull commands

27-Git Pull

    git pull \# Fetch changes from the remote repository and merge them into the current branch

28-Git Fetch

    git fetch <remote> <branch> \# Download updates from a remote branch to your local repository without merging them, allowing you to review changes before integrating

    { git pull == git fetch && git merge }

    















