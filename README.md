#To Do: Tried the git commands covered in class

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git remote -v
origin  https://github.com/Jasmine-tech17/Git_Practice.git (fetch)
origin  https://github.com/Jasmine-tech17/Git_Practice.git (push) 

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git add git_task1.txt 

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "First commit"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'ADMIN@DESKTOP-395LRC7.(none)')

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git config --global user.email "jasminechaudhary1997@gmail.com"

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git config --global user.name "Jasmine-tech17"

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "First commit"
[main (root-commit) dc40ff6] First commit
 1 file changed, 2 insertions(+)
 create mode 100644 git_task1.txt

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git branch
* main

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git push origin main
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 270 bytes | 38.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Jasmine-tech17/Git_Practice.git
 * [new branch]      main -> main


ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git remote -v
origin  https://github.com/Jasmine-tech17/Git_Practice.git (fetch)
origin  https://github.com/Jasmine-tech17/Git_Practice.git (push) 

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git branch
* main

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        git_task2.txt

nothing added to commit but untracked files present (use "git add" to track)

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git checkout -b "demo"
Switched to a new branch 'demo'

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git branch -a
* demo
  main
  remotes/origin/main

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git add git_task2.txt 

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git commit -m "New branch commit"
[demo d728549] New branch commit
 1 file changed, 2 insertions(+)
 create mode 100644 git_task2.txt

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git push origin demo
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 358 bytes | 39.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'demo' on GitHub by visiting:
remote:      https://github.com/Jasmine-tech17/Git_Practice/pull/new/demo
remote:
To https://github.com/Jasmine-tech17/Git_Practice.git
 * [new branch]      demo -> demo

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git log --oneline
d728549 (HEAD -> demo, origin/demo) New branch commit
dc40ff6 (origin/main, main) First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git add .

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git commit -m "Edited file"
[demo faa766d] Edited file
 1 file changed, 2 insertions(+), 2 deletions(-)

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git push origin demo
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 341 bytes | 113.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Jasmine-tech17/Git_Practice.git
   d728549..faa766d  demo -> demo

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git log --oneline
faa766d (HEAD -> demo, origin/demo) Edited file
d728549 New branch commit
dc40ff6 (origin/main, main) First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git log --oneline
dc40ff6 (HEAD -> main, origin/main) First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git merge demo
Updating dc40ff6..faa766d
Fast-forward
 git_task2.txt | 2 ++
 1 file changed, 2 insertions(+)
 create mode 100644 git_task2.txt

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git log --oneline
faa766d (HEAD -> main, origin/demo, demo) Edited file
d728549 New branch commit
dc40ff6 (origin/main) First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git log demo  --oneline
faa766d (HEAD -> main, origin/demo, demo) Edited file
d728549 New branch commit
dc40ff6 (origin/main) First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git log --oneline
faa766d (HEAD -> main, origin/demo, demo) Edited file
d728549 New branch commit
dc40ff6 (origin/main) First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git branch
  demo
* main

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git add .

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "Trying rebase"
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "Trying rebase"
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git_task2.txt

no changes added to commit (use "git add" and/or "git commit -a")

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git add .

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "Trying rebase"
[main 6d53334] Trying rebase
 1 file changed, 2 insertions(+), 2 deletions(-)

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git add .

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "rebase trial 2"
[main 5c6fb7b] rebase trial 2
 1 file changed, 2 insertions(+), 2 deletions(-)

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git add .

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git commit -m "rebase final"
[main 21f4595] rebase final
 1 file changed, 2 insertions(+), 2 deletions(-)

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git push origin main
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (9/9), 856 bytes | 214.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Jasmine-tech17/Git_Practice.git
   dc40ff6..21f4595  main -> main

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git log --oneline
21f4595 (HEAD -> main, origin/main) rebase final
5c6fb7b rebase trial 2
6d53334 Trying rebase
faa766d (origin/demo, demo) Edited file
d728549 New branch commit
dc40ff6 First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (main)
$ git checkout demo 
Switched to branch 'demo'

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git rebase main
Successfully rebased and updated refs/heads/demo.

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git push origin demo
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Jasmine-tech17/Git_Practice.git
   faa766d..21f4595  demo -> demo

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git log --oneline
21f4595 (HEAD -> demo, origin/main, origin/demo, main) rebase final
5c6fb7b rebase trial 2
6d53334 Trying rebase
faa766d Edited file
d728549 New branch commit
dc40ff6 First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git cherry-pick 6d5333
Auto-merging git_task2.txt
CONFLICT (content): Merge conflict in git_task2.txt
error: could not apply 6d53334... Trying rebase
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
hint: Disable this message with "git config advice.mergeConflict false"

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo|CHERRY-PICKING)
$ git add .

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo|CHERRY-PICKING)
$ git cherry-pick --continue
[demo 77cfc9c] Trying rebase
 Date: Fri Aug 9 00:41:29 2024 +0530
 1 file changed, 3 insertions(+), 2 deletions(-)

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git log --onelie
fatal: unrecognized argument: --onelie

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$ git log --oneline
77cfc9c (HEAD -> demo) Trying rebase
21f4595 (origin/main, origin/demo, main) rebase final
5c6fb7b rebase trial 2
6d53334 Trying rebase
faa766d Edited file
d728549 New branch commit
dc40ff6 First commit

ADMIN@DESKTOP-395LRC7 MINGW64 ~/guvi-practice/git_workspace/Git_Practice (demo)
$
