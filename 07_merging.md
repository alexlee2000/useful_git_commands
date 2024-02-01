# 7. Merging
1. Perform a **Fast-Forward Merge** (E.g. featureX is ready to be merged into the master branch)
```
git checkout master
git merge featureX
```

2. Perform a merge with a **Merge Commit**
```
git checkout master
git merge --no-ff featureX
```
