# change email

## References
* https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History
* http://git-memo.readthedocs.org/en/latest/filter-branch.html

### Pull from one repo and push to another
* Create a local project directory
* Initialize the project directory
* Configure the correct user name and email
* Add the first remote repository as origin
* Pull the project from origin
* Filter the branch
```
git filter-branch --commit-filter '
        if [ "$GIT_AUTHOR_EMAIL" = "old@emailaddres.example" ];
        then
                GIT_AUTHOR_EMAIL="new.email@address.eexample";
                git commit-tree "$@";
        else
                git commit-tree "$@";
        fi' HEAD
```
* Add the second remote repository as newhome
* Push the master branch to newhome

