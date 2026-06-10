## readme
```bash

bizim@BIZIMUNGU MINGW64 ~/myproject (main)
$ git init
Reinitialized existing Git repository in C:/Users/bizim/myproject/.git/

bizim@BIZIMUNGU MINGW64 ~/myproject (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ ls
services.html

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore.txt
        deleted:    README.md
        deleted:    app.js
        deleted:    blue.scc
        deleted:    index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

no changes added to commit (use "git add" and/or "git commit -a")

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git init
Reinitialized existing Git repository in C:/Users/bizim/myproject/.git/

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    .gitignore.txt
        deleted:    README.md
        deleted:    app.js
        deleted:    blue.scc
        deleted:    index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

no changes added to commit (use "git add" and/or "git commit -a")

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git add .

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    .gitignore.txt
        deleted:    README.md
        deleted:    app.js
        deleted:    blue.scc
        deleted:    index.html
        new file:   services.html


bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git commit -m "First commit"
[ft/bundle-2 4a16408] First commit
 6 files changed, 11 insertions(+), 19 deletions(-)
 delete mode 100644 .gitignore.txt
 delete mode 100644 README.md
 delete mode 100644 app.js
 delete mode 100644 blue.scc
 delete mode 100644 index.html
 create mode 100644 services.html

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git push origin ft/bundle-2
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git remote add origin https://github.com/Jpaulb12/git-exercises.git

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 22, done.
Counting objects: 100% (22/22), done.
Delta compression using up to 8 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (22/22), 2.00 KiB | 1022.00 KiB/s, done.
Total 22 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), done.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Jpaulb12/git-exercises/pull/new/ft/bundle-2
remote:
To https://github.com/Jpaulb12/git-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

bizim@BIZIMUNGU MINGW64 ~/myproject (ft/bundle-2)


```