# 6. Branches
1. **Create** and **Checkout** a branch
```
git branch featureA
git checkout featureA
```

2. **Checkout** an old commit (use git log to check that you are on the correct branch and HEAD --> featureA. Or you can do git branch to see which branch you are on) 
```
git log --oneline --graph --all
git checkout HEAD~
```

3. **Delete** a Branch (```-d``` might prompt you to confirm if the branch has not been merged. If you are happy to delete, then do ```-D```)
```
git branch -d featureA
git branch -D featureA
```

4. Immediately **undo** a Deletion of a Branch (reflog will show you local history of HEAD references. Find the SHA-1 of your most recent featureA branch here)
```
git reflog
git checkout -b featureA <SHA-1 you copied>
```
