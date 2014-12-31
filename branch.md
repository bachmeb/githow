###git branch
```
$ git branch
* master

$ git branch -a
* master
  origin/1-2-stable
  origin/2-0-stable
  origin/2-1-stable
  origin/2-2-stable
  origin/3-0-unstable
  origin/HEAD
  origin/master

$ git branch -r
  origin/1-2-stable
  origin/2-0-stable
  origin/2-1-stable
  origin/2-2-stable
  origin/3-0-unstable
  origin/HEAD
  origin/master
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
Brians-MacBook-Air:ost b$ 

```

[reference](http://gitready.com/intermediate/2009/02/13/list-remote-branches.html)
