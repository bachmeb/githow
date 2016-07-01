###git reset

## References
* http://stackoverflow.com/questions/1628088/how-to-reset-my-local-repository-to-be-just-like-the-remote-repository-head
* http://stackoverflow.com/questions/6006737/git-merge-errors

##### Hard reset
```
git commit -a -m "Saving my work, just in case"
git branch my-saved-work
git fetch origin
git reset --hard origin/master
```

##### Fix merge errors by resetting
```
git reset --merge
```



