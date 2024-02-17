# 9. Fetch, Pull, and Push
1. Network commands will allow Git to realize any new commits to a remote repo. If you want to fetch the latest commits from the remote repo, then use.
```
git fetch
```

2. If you want to update your local branches with any new changes in the remote repo, then use git pull. This will be a fast-forward merge if you haven't made any new commits on your local repo. Otherwise, the pull will be a merge-commit which will combine the work on your local repo with what has changed in the remote repo. 
```
git pull
```

3. You will be able to push your commits to the remote repo given that you have resolved any conflicts. The local and tracking branches will now be synchonized.
```
git push
```
