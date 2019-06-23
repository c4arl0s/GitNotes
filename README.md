# GitNotes

These are my personal notes about my knowledge of git and github

# Cloning a project from github

``` console
$ git clone https://github.com/c4arl0s/GitNotes.git
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
Enumerating objects: 32, done.
Counting objects: 100% (32/32), done.
Delta compression using up to 4 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (24/24), 4.43 KiB | 1.11 MiB/s, done.
Total 24 (delta 8), reused 0 (delta 0)
remote: Resolving deltas: 100% (8/8), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/c4arl0s/GitNotes.git
To https://github.com/carlos-santiago-2017/GitNotes.git
   a693336..5ec5521  master -> master
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

# Checking the logs of the repository

``` console
$ git log
commit a68832739bda48569016e08a0cec0c0be0b81a8d (HEAD -> master, origin/master, origin/HEAD)
Author: Carlos Santiago <c.santiago.cruz@gmail.com>
Date:   Sat Jun 22 20:15:09 2019 -0600

    Update README.md

commit d1593c4a5180f598115738476f479b38623a72f7
Author: Carlos Santiago <c.santiago.cruz@gmail.com>
Date:   Sat Jun 22 20:13:59 2019 -0600

    Update README.md

commit c9b538dc457598a6b2365407246801a83093f1d7
Author: Carlos Santiago <c.santiago.cruz@gmail.com>
Date:   Sat Jun 22 20:10:14 2019 -0600

    Update README.md

commit 5ec55216217e03d92577cce56ed6430817973c13
Merge: a9c4b0a a693336
:...skipping...
commit a68832739bda48569016e08a0cec0c0be0b81a8d (HEAD -> master, origin/master, origin/HEAD)
Author: Carlos Santiago <c.santiago.cruz@gmail.com>
Date:   Sat Jun 22 20:15:09 2019 -0600

    Update README.md

```

# List all the branches created

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
Switched to branch 'newBranch'
```

# What if you want to drop the last changes

``` console
git stash
```

``` console
gits stash drop
```

# What if you want to force to change what you did in local repository and overwrite remote repository, you first received a warning that you cannot push the changes, then add -f option

``` console
$ git push origin master
To https://github.com/carlos-santiago-2017/GitNotes.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/carlos-santiago-2017/GitNotes.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
Sat Jun 22 ~/Documents/SWIFT-PROGRAMMING/GitNotes 
$ git push -f origin master
Enumerating objects: 91, done.
Counting objects: 100% (91/91), done.
Delta compression using up to 4 threads
Compressing objects: 100% (90/90), done.
Writing objects: 100% (91/91), 18.91 KiB | 1.45 MiB/s, done.
Total 91 (delta 27), reused 0 (delta 0)
remote: Resolving deltas: 100% (27/27), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/c4arl0s/GitNotes.git
To https://github.com/carlos-santiago-2017/GitNotes.git
 + 4f71d1b...e488dc6 master -> master (forced update)
```

# View an Old version

``` console
$ git checkout 5ec5521
Note: checking out '5ec5521'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b <new-branch-name>

HEAD is now at 5ec5521 fix readme file
```


