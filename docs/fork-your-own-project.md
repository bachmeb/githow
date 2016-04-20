# fork your own project

## References
* http://bitdrift.com/post/4534738938/fork-your-own-project-on-github

##### 
* Create a new project on GitHub called 'whatever’
* Clone the existing project using the name 'whatever'
```
git clone git@github.com:YOURNAME/existing-project-name.git whatever
```
```
Initialized empty Git repository in /git/whatever/.git/
remote: Counting objects: 3618, done.
remote: Compressing objects: 100% (1503/1503), done.
remote: Total 3618 (delta 2629), reused 2922 (delta 2075)
Receiving objects: 100% (3618/3618), 7.31 MiB | 1.23 MiB/s, done.
Resolving deltas: 100% (2629/2629), done.
```
* Edit your Git config file
```
cd whatever
vim .git/config
```
* Replace the origin URL with your new URL:
```
[remote "origin"]
    fetch = +refs/heads/*:refs/remotes/origin/*
    url = git@github.com:YOURNAME/whatever.git #replace foo with whatever
```
* Push your new repository up to GitHub:
```
git push -u origin master
```
```
Counting objects: 3618, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (949/949), done.
Writing objects: 100% (3618/3618), 7.31 MiB | 646 KiB/s, done.
Total 3618 (delta 2629), reused 3618 (delta 2629)
To git@github.com:YOURNAME/whatever.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
```
