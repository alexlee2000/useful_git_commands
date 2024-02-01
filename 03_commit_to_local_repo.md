# 3. Committing to a Local Repo
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/2e18d4b2-f365-4c89-b348-635b9fa4a92d)

1. Create an empty file in your git repo
```
$ touch fileA.txt
```

2. Check for any changes in the repo (Checking whether a file is staged or is still untracked)
```
$ git status
```

3. Staging files that you want to commit
```
$ git add fileA.txt
```

4. Committing staged files (```-m``` Is an optional flag that will allow you to put in a commit message)
```
$ git commit -m "add fileA.txt"
```

5. View commit history
```
$ git log
$ git log --oneline
```
