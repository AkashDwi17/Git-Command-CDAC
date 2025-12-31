PS D:\Git-Practice> git init
Initialized empty Git repository in D:/Git-Practice/.git/
PS D:\Git-Practice> 



PS D:\Git-Practice> git status
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

nothing added to commit but untracked files present (use "git add" to track)
PS D:\Git-Practice>




PS D:\Git-Practice> git add Readme.md
warning: in the working copy of 'Readme.md', CRLF will be replaced by LF the next time Git touches it
PS D:\Git-Practice> 



PS D:\Git-Practice>  git commit -m "Add Readme.md File"
[master (root-commit) 8ef6779] Add Readme.md File
 1 file changed, 19 insertions(+)
 create mode 100644 Readme.md
PS D:\Git-Practice> 




PS D:\Git-Practice> git diff
warning: in the working copy of 'Readme.md', CRLF will be replaced by LF the next time Git touches it
diff --git a/Readme.md b/Readme.md
index 8c2a5de..99b683d 100644
--- a/Readme.md
+++ b/Readme.md
@@ -17,3 +17,18 @@ PS D:\Git-Practice>
 
 
:

PS D:\Git-Practice>  git log
commit 8ef6779793cd58d9e1fc39a06f4e4c8d4517ee88 (HEAD -> master)
Author: Akash Dwivedi <akashdwi17@gmail.com>
Date:   Wed Dec 31 11:50:49 2025 +0530

    Add Readme.md File
PS D:\Git-Practice> 




PS D:\Git-Practice> git branch
* master
PS D:\Git-Practice> 



PS D:\Git-Practice> git checkout
M       Readme.md
PS D:\Git-Practice> 


PS D:\Git-Practice> git checkout -b practice
Switched to a new branch 'practice'
PS D:\Git-Practice> 


PS D:\Git-Practice>  git switch practice
M       Readme.md
Already on 'practice'
PS D:\Git-Practice> 



PS D:\Git-Practice>  git switch master  
M       Readme.md
Switched to branch 'master'
PS D:\Git-Practice> 



PS D:\Git-Practice> git merge practice
Already up to date.
PS D:\Git-Practice> 


git restore :--  It is used to get back the last commit which is add i the repository


PS D:\Git-Practice> git reset
Unstaged changes after reset:
M       Readme.md
PS D:\Git-Practice> 

## What does git stash do?

git stash temporarily saves (shelves) your uncommitted changes (both staged and unstaged) and reverts your working directory to a clean state, so you can safely switch branches or work on something else.

## git stash stores uncommitted changes in a stack and restores the working directory to the last committed state.

PS D:\Git-Practice> git stash
warning: in the working copy of 'Readme.md', CRLF will be replaced by LF the next time Git touches it
Saved working directory and index state WIP on master: 8ef6779 Add Readme.md File
PS D:\Git-Practice> 

PS D:\Git-Practice> git remote
PS D:\Git-Practice> git remote -v



PS D:\Git-Practice> git remote add origin https://github.com/AkashDwi17/Git-Command-CDAC.git
PS D:\Git-Practice> git remote -v
origin  https://github.com/AkashDwi17/Git-Command-CDAC.git (fetch)
origin  https://github.com/AkashDwi17/Git-Command-CDAC.git (push)
PS D:\Git-Practice> git branch
* master
  practice
PS D:\Git-Practice> git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
PS D:\Git-Practice> 



PS D:\Git-Practice> git add .
warning: in the working copy of 'Readme.md', CRLF will be replaced by LF the next time Git touches it
PS D:\Git-Practice> git commit -m "Add Git Practice Readme.md File"
[master 177cd66] Add Git Practice Readme.md File
 1 file changed, 114 insertions(+)
PS D:\Git-Practice> 




PS D:\Git-Practice> git push origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 3.79 KiB | 3.79 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/AkashDwi17/Git-Command-CDAC.git
 * [new branch]      master -> master
PS D:\Git-Practice> 



PS D:\Git-Practice> git branch
* master
  practice
PS D:\Git-Practice> git remote -v
origin  https://github.com/AkashDwi17/Git-Command-CDAC.git (fetch)
origin  https://github.com/AkashDwi17/Git-Command-CDAC.git (push)
PS D:\Git-Practice> git branch --set-upstream-to=origin/master
branch 'master' set up to track 'origin/master'.
PS D:\Git-Practice> 
PS D:\Git-Practice> git pull
Already up to date.
PS D:\Git-Practice> 
PS D:\Git-Practice> 