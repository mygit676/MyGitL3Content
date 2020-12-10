# Demo for Fast-Forward Merge

1) Create a local git repository in your work-station
```
git init
```
2) Create some files . Lets say file1.html and file2.html 

3) Add and commit the files 

```
git add .
git commit -m "files"
```

4)  Run git log to view the commit-id
```
git log
```

5) Add another file file3.html and repeat the above steps. However, when running the commit command, provide a different message 

6) Create a new branch and checkout to it 

``` 
git checkout -b branch1

```
7) You will see the files from master copied to the branch. Create a new file called branchfile1.html

8) Add and commit again with a different commit message

9) Run git log. You will observe that the commits pointed by the master and different than the commits pointed by the branch 

10) Now, lets checkout to our master
```
git checkout master
```

11)Merge the branch1 to master

```
git merge branch1
```

You will see an output as below:

```
Updating 089da6e..2f12be6
Fast-forward
 branchfile1.html | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 branchfile1.html
```




