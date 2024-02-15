# 0. Most Used Git Commands (WIP)

List branches in the repo, or create a new branch, or see what branch you are on
```
git branch
```

Switch to a specific branch
```
git checkout
```

Check to see if there are any changes to files and which ones are currently staged for commit
```
git status
```

Stage files to be commited
```
git add <filepath>
git add --all
```

Committing changes locally
```
git commit -m "..."
```

Pushing changes to a remote repo for others to see
```
git push origin <branch>
```

Viewing commit history
```
git log --oneline
```

Merging your colleagues changes into your own branch
```
git checkout my_branch
git merge colleague_branch
```

# Case: Merging Branches with Colleagues

I have been working on a branch called ```AL_dev```. A colleague of mine (CF) has also made some changes to his branch ```CF_dev``` since we last merged. Before I submit a Pull Request (PR) into the master branch, I generally want to checkout ```CF_dev``` and use ```git status``` to see if there are any modifications CF has made that I can pull in before submitting the PR to master. If it says that the branch is up to date, then you can safely continue to push your changes to the remote repo and then submit a PR accordingly. 

On the other hand, if there has been commits to ```CF_dev``` since the last time that we merged, then the terminal will let you know by how many commits you are behind. Simply do ```git pull``` to pull in the modifications that CF has made. After that, you can ```git checkout AL_dev``` and then merge in CF's changes to your branch by doing ```git merge CF_dev```. In the case that you are both working on the same files, there may be some merge conflicts which will result in a failed merge. No problems. The terminal should indicate to you which files the merge failed on. Go to those files and look for something like:
```
def function()->Dataframe:
  print("Hello world")
  <<<<<<< HEAD
  #this is some content from AL_dev that I made
  =======
  #this is some content from CF_dev that CF made
  >>>>>>>
  return 0
```
Here we can see that I have put in some content and CF has also put in some content in the same section of the same file. Simply just resolve this conflict by replacing the conflicts with what is actually correct. E.g.
```
def function()->Dataframe:
  print("Hello world")
  #this is some content from AL_dev that I made
  return 0
```
Once you have resolved all conflicts, you can simply just stage those files again by doing ```git add <file>``` or ```git add --all``` to just add all files. Now, you can complete the merge by doing ```git commit -m "merge with CF_dev and resolve conflict in fileA.py"```. Now you have merged CF_dev into AL_dev!

Next, to make this visible in the remote repo for others to see, you should push origin <branch> ```git push origin alex_dev```. This will push your changes to the remote repo on bitbucket and now your colleagues can see your merge commit. To now bring both of your changes into the master branch, you can simply raise a PR on bitbucket and set the reviewer. Once they have reviewed and have no problems with your PR, they will pull the changes into the master branch.
