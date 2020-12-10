# Conflict Demo

1) Let us assume a file "file1.txt" in our codecommit repo. The file has the following content. followinf content

```
This is a demo for merge conflict
This is console-user
```

2) Clone this repo onto your workstation .  Checkout to a new branch and Modify the file as

```
This is a conflictdemo
This is console-user
This is change1
```
3) Now , for the sake of demo, let us chaneg the file in codecommit to 

```
This is a conflictdemo2
This is console-user
change2 is this
```
4) Create pull request from the console
5) We encounter conflicts now.

# Resolution

1) Pull changed from remote to local workstation  , in order to resolve the conflicts
2) In the branch, run 
```
git pull origin master 
```
3) We run into merge conflicts
4) Open the file. We notice the markers added by git 
5)Remove the markers and save the file
6)Add, Commit and  Push the changes to the remote branch 
7) Now, we will be able to successfully merge the branches.
