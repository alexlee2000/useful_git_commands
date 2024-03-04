# 10. Rebasing (Rewriting history)
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/1db591fd-da5d-4ea9-83c5-eaa69ce6ac97)

1. Rebase the commit on featureX branch to the tip of the master branch
```
git checkout featureX
git rebase master
```

2. Rebase when there is a merge conflict
```
git checkout featureX
git rebase master
...a.   conflict
git status
...a.   both modified fileA.txt
...fix fileA.txt
git add fileA.txt
git rebase --continue
```

3. Rewriting history - Changing contents of a file + Changing commit message
```
git commit --ammend -m "ammended commit message"
```
  
5. Rewriting history - Removing a commit using Interactive Rebase
```
git rebase -i <SHA-1>
...An interactive rebase editor should open
...Change 'pick' command to 'squash'
...Verify that the commit has been removed
...Merge the branch which you deleted from and delete its branch label
```
6. Rewriting history - Squash merge

![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/d2ca6de5-6fa9-4091-a9b5-8ffb5e256501)
-	Merges the tip of the feature branch (D) onto the tip of the base branch (C). There is a chance of a merge conflict.
```
git checkout master
git merge --squash featureX
git commit -m "add featureX"
```

