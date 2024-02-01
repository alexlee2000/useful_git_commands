# 4. Push to Remote Repo
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/1c96eaef-052c-4ebc-ac88-34a87259cf58)

1. **Clone** a Bitbucket repository
```
$ git clone 
```

2. Create a **commit** in the local repository by first adding to staing area and then checking that the file is staged.
```
$ git add FileB.txt
$ git status
$ git commit -m "Add FileB.txt"
```

3. **Push** the commit to the remote repository
```
$ git push -u origin master
$ git status
```
