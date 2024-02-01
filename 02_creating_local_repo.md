# 2. Creating a Local Repo
![image](https://github.com/alexlee2000/useful_git_commands/assets/43845085/b79f0c5b-43f2-472a-8e93-3c2571f21a2b)

1. Change to your user directory (or wherever you want to place the new directory)
```
$ cd
$ cd <directory_path>
```

2. Create a new directory and initialize a repository
```
$ mkdir new_directory  
$ cd new_directory
$ git init
Initialized empty Git repository in new_directory/.git/
```

3. Verify that your new_directory contains a ```.git``` directory 
```
$ ls - a
. .. .git
```
