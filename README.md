# GitNotes

These are my personal notes about my knowledge of git and github

# Cloning a project from github

``` console
$ git clone https://github.com/c4arl0s/FastEnumeration_ObjectiveC.git
```
# Checking the status of the repository

``` console
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

# Adding all the current changes to the local repostory for all files, you can also add one single file.

``` console
$ git add .
```

# Pulling the changes from github master branch

``` console
$ git pull origin master
```

# Pushing the changes from local repository to remote repository

``` console
$ git push origin master
```

# git reset

``` console
git reset --hard <commit-hash>
git push -f origin master
```

# What if you want to drop the last changes

``` console
$ git stash
```

``` console
$ gits stash drop
```

# list all the branches created

At this point, it shows only master. Take a look.

``` console
$ git brach
* master
```

# Create a new branch called newBranch

``` console
$ git branch newBranch
```

``` console
$ git branch
* master
  newBranch
```

# Once you create the branch, change to the new branch. Use checkout command.

``` console
$ git checkout newBranch
```










