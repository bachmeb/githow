# git branch

## References
* https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging
* http://gitready.com/intermediate/2009/02/13/list-remote-branches.html
* https://backlogtool.com/git-guide/en/stepup/stepup1_3.html
* https://git-scm.com/docs/git-branch
* http://kb.detlus.com/articles/git/how-to-update-remote-branch-list-on-local-machine/

### Notes
* When you switch branches, Git resets your working directory to look like it did the last time you committed on that branch. (https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

##### Which branch do I have checked out?
```
git branch
```
```
* master
```

##### List branches and show both local and remote branches
```
$ git branch -a
```
```
* master
  origin/1-2-stable
  origin/2-0-stable
  origin/2-1-stable
  origin/2-2-stable
  origin/3-0-unstable
  origin/HEAD
  origin/master
```

##### List remote branches
```
$ git branch -r
  origin/1-2-stable
  origin/2-0-stable
  origin/2-1-stable
  origin/2-2-stable
  origin/3-0-unstable
  origin/HEAD
  origin/master
```



##### Create a new branch head named [branchname] which points to the current HEAD
```
git branch new_branch_name
```

##### Switch to the new branch
```
git checkout new_branch_name
```

```
System:ost b$ git checkout origin/java/3/lesson/13
Note: checking out 'origin/java/3/lesson/13'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at 523879b... add CardImage
System:ost b$ git checkout -b java/3/lesson/13
Switched to a new branch 'java/3/lesson/13'
System:ost b$ 
```

##### Create a branch and check it out with a single command
```
git checkout -b new_branch_name
```

##### Update local list of remote branches
```
git remote update origin --prune
```
