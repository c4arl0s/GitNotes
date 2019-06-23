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

# Adding all the current changes from local repostory for all files, you can also add one single file.

``` console
$ git add .
```

# Commiting the last change

``` console
$ git commit -m "Add a few changes"
```

# Pushing the changes from local repository to remote repository

``` console
$ git push origin master
```

# Pulling the changes from github master branch

``` console
$ git pull origin master
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/carlos-santiago-2017/GitNotes
 * branch            master     -> FETCH_HEAD
   5ec5521..c9b538d  master     -> origin/master
Updating 5ec5521..c9b538d
Fast-forward
 README.md | 8 ++++----
 1 file changed, 4 insertions(+), 4 deletions(-)
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

# Once you created the new branch, change to that branch

``` console
$ git checkout newBranch


# git reset

``` console
git reset --hard <commit-hash>
git push -f origin master
```

# What if you want to drop the last changes

``` console
git stash
```

``` console
gits stash drop
```
