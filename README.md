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

## bundle 2 ex 1

```
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)olutions-2- (dev)
$ git branch ft/bundle-2
                                                   olutions-2- (dev)
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git commit -m "made some changes in ft/bundle-2 by adding a file"
[dev d15fc0f] made some changes in ft/bundle-2 by adding a file
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (dev)
$ git push origin dev
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 255 bytes | 255.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-.git
   19b49a0..d15fc0f  dev -> dev
```

## bundle 3 ex 1

```
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
  ft/bundle-2
  ft/service-redesign
* main

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
olutions-2- (ft/team-page)
$ touch team.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)  olutions-2- (ft/team-page)
$ ls
about.html  home.html  index.html  README.md  serviolutions-2- (ft/team-page)  ces.html  team.html
                                                   ces.html  team.html
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)                         olutions-2- (ft/team-page)
$ git status
On branch ft/team-page
nothing to commit, working tree clean

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ touch team2.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will
be committed)
        team2.html

nothing added to commit but untracked files present (use "git add" to track)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git coomit -m "create team2 file "
git: 'coomit' is not a git command. See 'git --help'.

The most similar command is
        commit

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git commit -m "create team2 file "
[ft/team-page e9fe327] create team2 file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 team2.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 269 bytes | 134.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused
0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-/pull/new/ft/team-page
remote:
To https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-.git
 * [new branch]      ft/team-page -> ft/team-page

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
$ git  branch ft/contact-page

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git log
commit e9fe3275cb93befbfd3757b6448079995aab04fa (HEAD -> ft/team-page, origin/ft/team-page)
Author: pothin-otf <pothinotf@gmail.com>
Date:   Thu May 22 20:23:05 2025 +0200

    create team2 file

commit c63370dc4b558bc71c1cac0c58bea233a84026a7 (origin/main, origin/HEAD, main, ft/contact-page)
Author: pothin-otf <pothinotf@gmail.com>
Date:   Thu May 22 16:25:50 2025 +0200

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git cherry-pick e9fe3275cb93befbfd3757b6448079995aab04fa
[ft/contact-page fe1423c] create team2 file
 Date: Thu May 22 20:23:05 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 team2.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git status
On branch ft/contact-page
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git commit -m "just used querry-pick"
[ft/contact-page 0d096c3] just used querry-pick
 1 file changed, 1 insertion(+)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 597 bytes | 199.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused
0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-/pull/new/ft/contact-page
remote:
To https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-.git
 * [new branch]      ft/contact-page -> ft/contact-page

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)olutions-2- (ft/contact-page)
$ git checkout ft/contact-page
Already on 'ft/contact-page'
                                                   olutions-2- (ft/contact-page)
One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git branch ft/faq-page                           olutions-2- (ft/contact-page)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/contact-page)
$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ touch faq.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ git status
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will
be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ git add .

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ git commit -m ::
[ft/faq-page 860800e] ::
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ git commit -m "added faq.html"
On branch ft/faq-page
nothing to commit, working tree clean

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 222 bytes | 111.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused
0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on
GitHub by visiting:
remote:      https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-/pull/new/ft/faq-page
remote:
To https://github.com/Pothin-Neza/Gym-Git-Exercise-Solutions-2-.git
 * [new branch]      ft/faq-page -> ft/faq-page

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/faq-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git log
commit e9fe3275cb93befbfd3757b6448079995aab04fa (HEAD -> ft/team-page, origin/ft/team-page)
Author: pothin-otf <pothinotf@gmail.com>
Date:   Thu May 22 20:23:05 2025 +0200

    create team2 file

commit c63370dc4b558bc71c1cac0c58bea233a84026a7 (origin/main, origin/HEAD, main)
Revert "create team2 file"
Author: pothin-otf <pothinotf@gmail.com>
Date:   Thu May 22 16:25:50 2025 +0200

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
$ git revert e9fe3275cb93befbfd3757b6448079995aab04fa
[ft/team-page 6ea125a] Revert "create team2 file"
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 team2.html

One plus Ltd@PothinN23 MINGW64 ~/Gym-Git-Exercise-Solutions-2- (ft/team-page)
```
