# 5. Tagging Commits
1. View References to a commit
```
$ git log --oneline
$ git show <first 4 characters of SHA-1 OR complete SHA-1)
$ git show HEAD
$ git show master
```

2. Viewing references to a commit's parent, grandparent, and 2nd parent in a merge commit respectively. 
```
$ git show HEAD~
$ git show HEAD~2
$ git show HEAD^2
```

3. Tagging a commit, viewing it, and committing it to remote repo
```
$ git tag
$ git tag -a -m "Tag message here" <tag name here>
$ git show <tag name here>
$ git push origin <tag name here>
```

4. Tagging other commits, and deleting the tag
```
$ git tag -a -m  "Tag message here" <tag name here> HEAD~
$ git tag -d <tag name here>
```
