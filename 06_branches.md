# 6. Branches
1. **Create** and **Checkout** a branch (and push to remote repo upstream)
```
git branch featureA
git checkout featureA
git push -u origin featureA
```
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/bead4f96-bd41-42c4-8e8f-ad1a1042c5b9)


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
