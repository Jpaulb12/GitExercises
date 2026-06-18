## readme
### Bundle 1 Exercise2
``` bash

bizim@BIZIMUNGU MINGW64 ~ (main)
$ cd Desktop/GitStudy
bash: cd: Desktop/GitStudy: No such file or directory

bizim@BIZIMUNGU MINGW64 ~ (main)
$ cd OneDrive/Desktop/GitStudy

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git init
Initialized empty Git repository in C:/Users/bizim/OneDrive/Desktop/GitStudy/.git/

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git add .

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   home.html


bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ cat home.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hello my people</h1>
</body>
</html>
bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash push -u -m "home page"

You do not have the initial commit yet

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash list

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ ^C

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   home.html


bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git add .

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git commit -m "First commit"
[main (root-commit) 7957382] First commit
 1 file changed, 11 insertions(+)
 create mode 100644 home.html

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash push -u -m "Home page"
No local changes to save

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ ^C

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status

On branch main
nothing to commit, working tree clean

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ ls -la
total 13
drwxr-xr-x 1 bizim 197609   0 Jun 18 13:02 ./
drwxr-xr-x 1 bizim 197609   0 Jun 18 12:54 ../
drwxr-xr-x 1 bizim 197609   0 Jun 18 13:06 .git/
-rw-r--r-- 1 bizim 197609 239 Jun 18 13:01 home.html

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash push -u -m "Home page"
Saved working directory and index state On main: Home page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash list
stash@{0}: On main: Home page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash push -u -m "about page"
Saved working directory and index state On main: about page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash list
stash@{0}: On main: about page
stash@{1}: On main: Home page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash push -u -m "team page"
Saved working directory and index state On main: team page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash list
stash@{0}: On main: team page
stash@{1}: On main: about page
stash@{2}: On main: Home page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash pop stash@{0}
Already up to date.
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (999e0db2b16e8eb7b806364f5c48934709db76da)

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash list
stash@{0}: On main: about page
stash@{1}: On main: Home page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash pop stash@{1}
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (163870189c6b0612d0f559eea68e9e4d483f6e71)

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

no changes added to commit (use "git add" and/or "git commit -a")

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git add .

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ gir commit -m "Restoring home about and team pages from stash"
bash: gir: command not found

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git commit -m "Restoring home about and team pages from stash"
[main 67ccc42] Restoring home about and team pages from stash
 2 files changed, 12 insertions(+)
 create mode 100644 team.html

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git push origin main
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git remote -v

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git remote add origin https://github.com/Jpaulb12/gitExercises2.git

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git remote -v
origin  https://github.com/Jpaulb12/gitExercises2.git (fetch)
origin  https://github.com/Jpaulb12/gitExercises2.git (push)

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 774 bytes | 774.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/Jpaulb12/gitExercises2.git
 * [new branch]      main -> main

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)
$ git stash list
stash@{0}: On main: about page

bizim@BIZIMUNGU MINGW64 ~/OneDrive/Desktop/GitStudy (main)

```