#  Json_GIT_Homework 1

## 1. Create an external repository called JSON on Github site.
I go to https://github.com/MariaDash, click "Repositories", click "New", make it Public, add README.md file, create repository.
## 2. Clone repository to local PC
I go to repository page--> Code --> Local and copy its link. And here two options: 
You can copy by HTTPS( unsecure without password) or SSH (need specific configuration and it is secure and always ask password).. I copy via HTTPS.
On PC I go to my folder "GIT", right click "Gitbash Here" and open a terminal Gitbash in this folder.
```

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git (main)
$ git clone https://github.com/MariaDash/Json.git
Cloning into 'Json'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git (main)
$cd Json
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ ls 
README.md

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
Note: if you need to change your working repository:
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$git remote set-url origin https://github.com/MariaDash/Json.git

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git remote -v
origin  https://github.com/MariaDash/Json.git (fetch)
origin  https://github.com/MariaDash/Json.git (push)
```

## 3. Create new.json file in the local repo.
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
## 4.  Add a file for tracking
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
## 5. Do commit it.
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
## 6. Send the file to remote repository

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
## 7. Edit the content of the “new.json” file - write information about yourself (full name, age, number of pets, future desired salary). Everything is written in JSON format.
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
## 8. Send the changes to remote repository
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
Note: Here I had a conflict between remote and local repository so I first needed to pull the remote version (and add a commit message) and after this I can push the local version to the remote repo.
## 9. Create preferences.json file.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ cat > preferences.json


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ ls
README.md  new.json  preferences.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 10. In the preferences.json file, add information about your preferences (Favorite movie, favorite series, favorite food, favorite season, side you would like to visit) in JSON format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ vim preferences.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ cat preferences.json
{

  "favorite movie": "G.I. Jane" ,
  "favorite tv show": "Friends",
  "favorite food": " wok" ,
  "favorite season of the year": "Winter",
  "Country to travel": "Italy"


}


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 11. Create a file skills.json add information about the skills that will be studied in the course in JSON format.

```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ vim skills.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ cat skills.json
{

  "skills":
  ["SQL", "Postman", "Git", "Terminal", "DevTools", "Jmeter", "Fiddler", "Charles Proxy", "ADB"]






}

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 12. Send 2 files at once to an external repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        preferences.json
        skills.json

nothing added to commit but untracked files present (use "git add" to track)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git add .
warning: in the working copy of 'preferences.json', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'skills.json', LF will be replaced by CRLF the next time Git touches it

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   preferences.json
        new file:   skills.json


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git commit -m
error: switch `m' requires a value

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git commit -m "two files"
[main c612ced] two files
 2 files changed, 22 insertions(+)
 create mode 100644 preferences.json
 create mode 100644 skills.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 936 bytes | 468.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/Json.git
   d5b2111..b84acc9  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
## 13. On the web interface, create a bug_report.json file.
## 14. Make Commit changes (save) changes on the web interface.
## 15. On the web interface, modify the bug_report.json file, add a bug report in JSON format.
## 16. Make Commit changes (save) changes on the web interface.
## 17. Synchronize external and local JSON repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ git pull
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), 1.36 KiB | 81.00 KiB/s, done.
From https://github.com/MariaDash/Json
   b84acc9..407a8e0  main       -> origin/main
Updating b84acc9..407a8e0
Fast-forward
 bug_report.json | 8 ++++++++
 1 file changed, 8 insertions(+)
 create mode 100644 bug_report.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ ls
README.md  bug_report.json  new.json  preferences.json  skills.json

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$ cat bug_report.json
{

"ID":1,
"Module": "LogIn",
"Severity": "Critical",
"Priority": "High",
"Title": "'Login' button disabled when pushing it after adding valid login & password",
"Test_Data":{
  "login":"Adam", 
  "password":"abc123"
   }
"Pre-condition": "user is registered",
"Env": ["Windows 10, Google Chrome 112",
       "Windows 10, Firefox",
       "Windows 10, Opera"],
"STR": {
      [ "1. Navigate to the site.com",
        "2. In the login block enter test data in 'login' and 'password' fields",
        "3. Push 'Login' button",
        "4. 'Login' button is disabled. No warning message."
        ]
  }
"ER": "'Login' button is enabled, user log in.",
"AR": "'Login' button is disabled. User can not log in.",
"Link_attach": "Link",
"Bug_started":"@me",
"Bug_Repro":"@someone_else"
  
  
  
}


Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/Json (main)
$
```
