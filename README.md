# # Json Homework 1
1-3 done
## 4. Create an external repository called JSON on Github site.
I go to https://github.com/MariaDash, click "Repositories", click "New", make it Public, add README.md file, create repository.
## 5. Clone repository to local PC
I go to repository page--> Code --> Local and copy its link. And here two options: 
You can copy by HTTPS( unsecure without password) or SSH (need specific configuration and it is secure and always ask password).. I cpoy via HTTPS.
On PC I go to my folder "Json", right click "Gitbash Here" and open a terminal Gitbash in this folder.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git remote set-url origin https://github.com/MariaDash/Json.git

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git remote -v
origin  https://github.com/MariaDash/Json.git (fetch)
origin  https://github.com/MariaDash/Json.git (push)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git clone https://github.com/MariaDash/Json.git
Cloning into 'Json'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ ls
README.md

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
Because I have already another repository I must swith it. As you can see the repository is cloned to PC.
## 6. Create new.json file in the local repo.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ vim new.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ cat new.json
{
  "name": "value"


}


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        new.json

nothing added to commit but untracked files present (use "git add" to track)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$

```
## 7.  Add a file for tracking
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git add new.json
warning: in the working copy of 'Json/new.json', LF will be replaced by CRLF the next time Git touches it

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new.json


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 8. Do commit it.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git commit -m "new.json creation"
[main a9fb950] new.json creation
 1 file changed, 5 insertions(+)
 create mode 100644 new.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
git log
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git log
commit a9fb950f540832b7f4c9a0789ee5119862dbc33a (HEAD -> main)
Author: MariaDash <mafunta@gmail.com>
Date:   Thu Apr 27 17:13:36 2023 +0300

    new.json creation

commit 88eec610db10ab7a3de608d9ed1295a0fb17811c (origin/main, origin/HEAD)
Author: MariaDash <122399261+MariaDash@users.noreply.github.com>
Date:   Thu Apr 27 17:04:49 2023 +0300

    Initial commit

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 9. Send the file to remote repository

```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 301 bytes | 100.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/Json.git
   88eec61..a9fb950  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 10. Edit the content of the “new.json” file - write information about yourself (full name, age, number of pets, future desired salary). Everything is written in JSON format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ vim new.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ cat new.json
{
  "name": "Mariia",
  "surname": "Dashkova",
  "age" : 35,
  "number of pets": 0,
  "desired salary": 1500


}

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 11. Send the changes to remote repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   new.json

no changes added to commit (use "git add" and/or "git commit -a")
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git add new.json
warning: in the working copy of 'new.json', LF will be replaced by CRLF the next time Git touches it

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git commit -m " changes in new.json"
[main ac97e4f]  changes in new.json
 1 file changed, 5 insertions(+), 1 deletion(-)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git push
To https://github.com/MariaDash/Json.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/MariaDash/Json.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git pull
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (9/9), 3.23 KiB | 67.00 KiB/s, done.
From https://github.com/MariaDash/Json
   a9fb950..f7174b7  main       -> origin/main
Merge made by the 'ort' strategy.
 README.md | 128 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 127 insertions(+), 1 deletion(-)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git push
Enumerating objects: 9, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 681 bytes | 340.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/Json.git
   f7174b7..ccae60e  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
Note: Here I had a conflict between remote and local repository so I first needed to pull the remote version and after this I can push the local version to the remote repo.
## 12 Create preferences.json file.

