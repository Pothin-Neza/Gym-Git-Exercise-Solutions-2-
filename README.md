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