# Basic Git Commands 

1) Initialize a local git repository :
```
git init
```

2) Cloning a repository 
```
git clone <url>
```

3) Checking if the local repository has a linked remote repository

```
git remote -v
```

4) Pushing to a remote repo 

```
git push <url>
```

5) Creating a branch 

```
git branch < new branch name>
```

6) Checking out to a new branch 

```
git checkout <branch>
```

7) Creating a new branch and checking out to it in one go 

```
git checkout -b <branch>
```

8) Merging a branch 
```
git merge <branch-name>
```

9) Checking all branches
```
git branch -a
```

10) Pushing files to a stashing directory 

```
git stash push [-m message]
```

11) Checking the log

``` 
git log
```

12) Checking the status
```
git status
```
13) Rebasing commits
```
git rebase

14)Pointer to the currently Checked out branch

git show HEAD
