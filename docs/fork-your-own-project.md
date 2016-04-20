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
Cloning into 'project-name'...
remote: Counting objects: 792, done.
remote: Total 792 (delta 0), reused 0 (delta 0), pack-reused 792
Receiving objects: 100% (792/792), 210.72 KiB | 0 bytes/s, done.
Resolving deltas: 100% (386/386), done.
Checking connectivity... done.
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
    url = git@github.com:YOURNAME/whatever.git #replace existing project name with whatever
```
* Push your new repository up to GitHub:
```
git push -u origin master
```
```
Counting objects: 792, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (277/277), done.
Writing objects: 100% (792/792), 210.72 KiB | 0 bytes/s, done.
Total 792 (delta 386), reused 792 (delta 386)
To git@github.com:bachmeb/whatever.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
```
