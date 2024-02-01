# 4. Push to Remote Repo
1. Clone a Bitbucket repository
```
$ git clone 
```

2. Create a commit in the local repository
```
$ git add FileB.txt
$ git commit -m "Add FileB.txt"
```

2.5. Check that the file is now staged 
```
$ git status
```

3. Push the commit to the remote repository
```
$ git push -u origin master
$ git status
```
