# Gym-Git-Exercise-Solutions-2-

## Bundle 1 Exercise 1

```

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.      

Untracked files:
  (use "git add <file>..." to include in what will 
be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
$ git branch
* main

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
$ git branch main master
fatal: a branch named 'main' already exists

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
$ git branch -m main master

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (master)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (master)
$ git commit -m "renamed main to master"
[master e2a2606] renamed main to master
 1 file changed, 11 insertions(+)
 create mode 100644 index.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (master)        
$ git remote add origin https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-.gitns-2-.git
error: remote origin already exists.

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (master)        
$ git push origin master
Enumerating objects: 4, done.      
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 429 bytes | 214.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-/pull/new/master
remote:
To https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-.git
 * [new branch]      master -> master

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (master)        
$ git branch dev

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (master)        
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git branch test
                                                   olutions-2- (dev)
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git branch -D test                               olutions-2- (dev)
Deleted branch test (was e2a2606).
```

## bundle 1 ex 2

```
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will 
be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash
No local changes to save

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash
No local changes to save

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)olutions-2- (dev)
$ git stash -u                                      a1410a6 done with exercise 
Saved working directory and index state WIP on dev: a1410a6 done with exercise 1 bundle 1
                                                   olutions-2- (dev)
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will 
be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)        new file:   about.html


One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash
Saved working directory and index state WIP on dev: a1410a6 done with exercise 1 bundle 1

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash
No local changes to save

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash -u
Saved working directory and index state WIP on dev: a1410a6 done with exercise 
1 bundle 1

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash list
stash@{0}: WIP on dev: a1410a6 done with exercise 1 bundle 1
stash@{1}: WIP on dev: a1410a6 done with exercise 1 bundle 1
stash@{2}: WIP on dev: a1410a6 done with exercise 1 bundle 1

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (9966766e7d615198f8c5a14c3bfcb8a5791e437c)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash pop stash@{0}
Already up to date.
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

Dropped stash@{0} (db68d71a70c827f0bc383d9a771baef9116fcc49)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git commit -m "unstashed about and home files"
[dev 69b61cc] unstashed about and home files
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 team.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash pop stash@{2}
fatal: log for 'stash' only has 1 entries

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash list
stash@{0}: WIP on dev: a1410a6 done with exercise 1 bundle 1

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git stash pop stash@{0}
Already up to date.
On branch dev
nothing added to commit but untracked files present (use "git add" to track)   
Dropped stash@{0} (6ddad511e39aa7237232ceec701ff2ed7202b4b5)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git reset
```