# 8. Tracking Branches
1. View the local and tracking branch names
```
git branch --all
```

2. View the combined log of all local and tracking branches. Make note of the labels you see for the branches. If you make a commit to the local repo, without pushing it to the remote repo, the local branch will be ahead of the tracking branch by X commits. The tracking branch only knows what the remote repository knows. 
- ```master```: Represents the tip of the master branch on the local repo
- ```origin/master```: Represents the tip of the master branch on the remote repo
- ```origin/HEAD```: Represents the tip of the default branch on the remote repo
```
git log --all --oneline --graph
```
