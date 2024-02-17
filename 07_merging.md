# 7. Merging
1. Perform a **Fast-Forward Merge** (E.g. featureX is ready to be merged into the master branch)
```
git checkout master
git merge featureX
```
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/2516f54b-46fd-46a9-881b-b265fa92a76c)

2. Perform a merge with a **Merge Commit**
```
git checkout master
git merge --no-ff featureX
```
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/43be1c95-2540-4cbc-961a-7c50d21a6421)

# 7.1. Resolving Merge Conflicts
1. In the case that there is a merge conflict, you can abort the merge process if you don't want to fix the conflict right now. 
```
git merge --abort
```

2. Or, you can fix the conflict and contiune the merge by modifying the conflicted files directly. Remove the conflict markers and make adjustments where necessary. 
