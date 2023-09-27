# Task 1
To see how I did the first task click the lincks below.⬇︎
 
 It contains description.
- [JSON](https://github.com/olyacenko/JSON)
- [XML](https://github.com/olyacenko/XML)
- [TXT](https://github.com/olyacenko/TXT)
-----
# Task 2
Precondidion:
 Create a remote repository => Go to GitHub account => click on the `new repository` button => enter Repository name => click on the `Public` button => click `Add a README file` => click on `Create repository` button => Clone the repository to the local computer => Go to the repository page => click on `Code` => `Local`=>  `SSH` => `Copy link` => on PC open terminal => enter command `mkdir git_hw_2` => `cd git_hw_2` => `git clone git@github.com:olyacenko/Git.git`
```
dmitrijostalskij@MacBook-Pro-2 hw_ksendzov_courses % mkdir git_hw_2
dmitrijostalskij@MacBook-Pro-2 hw_ksendzov_courses % cd git_hw_2
dmitrijostalskij@MacBook-Pro-2 git_hw_2 % git clone git@github.com:olyacenko/Git.git
Cloning into 'Git'...
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 18 (delta 2), reused 4 (delta 0), pack-reused 0
Receiving objects: 100% (18/18), 4.75 KiB | 1.19 MiB/s, done.
Resolving deltas: 100% (2/2), done.
dmitrijostalskij@MacBook-Pro-2 git_hw_2 % 
```
1. On the local repository create branches for:
    - Postman
    - Jmeter
    - CheckLists
    - Bug Reports
    - SQL
    - Charles
    - Mobile testing
```
dmitrijostalskij@MacBook-Pro-2 Git % git branch Postman
dmitrijostalskij@MacBook-Pro-2 Git % git branch Jmeter
dmitrijostalskij@MacBook-Pro-2 Git % git branch CheckLists
dmitrijostalskij@MacBook-Pro-2 Git % git branch Bug_Reports
dmitrijostalskij@MacBook-Pro-2 Git % git branch SQL        
dmitrijostalskij@MacBook-Pro-2 Git % git branch Charles
dmitrijostalskij@MacBook-Pro-2 Git % git branch Mobile_testing
dmitrijostalskij@MacBook-Pro-2 Git % git branch               
  Bug_Reports
  Charles
  CheckLists
  Jmeter
  Mobile_testing
  Postman
  SQL
* main
dmitrijostalskij@MacBook-Pro-2 Git % 
```
2. Push all branches to the remote repository.
```
dmitrijostalskij@MacBook-Pro-2 Git % git push -u origin Bug_Reports Charles CheckLists Jmeter Mobile_testing Postman SQL            
Total 0 (delta 0), reused 0 (delta 0)
To github.com:olyacenko/Git.git
 * [new branch]      Bug_Reports -> Bug_Reports
 * [new branch]      Charles -> Charles
 * [new branch]      CheckLists -> CheckLists
 * [new branch]      Jmeter -> Jmeter
 * [new branch]      Mobile_testing -> Mobile_testing
 * [new branch]      Postman -> Postman
 * [new branch]      SQL -> SQL
Branch 'Bug_Reports' set up to track remote branch 'Bug_Reports' from 'origin'.
Branch 'Charles' set up to track remote branch 'Charles' from 'origin'.
Branch 'CheckLists' set up to track remote branch 'CheckLists' from 'origin'.
Branch 'Jmeter' set up to track remote branch 'Jmeter' from 'origin'.
Branch 'Mobile_testing' set up to track remote branch 'Mobile_testing' from 'origin'.
Branch 'Postman' set up to track remote branch 'Postman' from 'origin'.
Branch 'SQL' set up to track remote branch 'SQL' from 'origin'.
dmitrijostalskij@MacBook-Pro-2 Git % 
```
3. In the Bug_Reports branch create a text document with the bug report structure.
```
dmitrijostalskij@MacBook-Pro-2 Git % git checkout Bug_Reports
Switched to branch 'Bug_Reports'
Your branch is up to date with 'origin/Bug_Reports'.

dmitrijostalskij@MacBook-Pro-2 Git % vim bug_report_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % cat bug_report_pattern.txt
id: 1 
title: issue with displaying an author's name on detailed story page of my-stories.
siverity/priority: minor/low
sttus: to do
assignee: front end developer
environment: [DEV|https://link-to-dev.web.app/login], Safari virsion 15.6.1
description: Author of a story can see own name and avatar on the detailed story page of my-stories. According to [Figma|https://www.figma.com/file] design author should not see own name
precondition: create your own story or use: username: ollyatsenko@example.com, password: 123456
STR: 
 1. Log in to the platform
 2. go to my-stories page
 3. tap on any story
 4. pay attention to the avatar and name of story's author under title of the story
AR: The author's name and avatar are displayed below the story's title.
ER: The author's name and avatar are not displayed below the story's title.
attachment: https://prnt.sc/vcm9PS5ZGmzd
dmitrijostalskij@MacBook-Pro-2 Git % 
```
4. Push the bug report structure to the remote repository.
```
dmitrijostalskij@MacBook-Pro-2 Git % git add bug_report_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % git commit -m "add file bug_report_pattern.txt"
[Bug_Reports 4879b51] add file bug_report_pattern.txt
 1 file changed, 16 insertions(+)
 create mode 100644 bug_report_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 780 bytes | 780.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:olyacenko/Git.git
   97cbc6b..4879b51  Bug_Reports -> Bug_Reports
dmitrijostalskij@MacBook-Pro-2 Git % 
```
5. Merge the Bug_Reports branch to main.
```
dmitrijostalskij@MacBook-Pro-2 Git % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

dmitrijostalskij@MacBook-Pro-2 Git % git merge Bug_Reports
Updating 97cbc6b..4879b51
Fast-forward
 bug_report_pattern.txt | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)
 create mode 100644 bug_report_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % 
```
6. Push main branch to the remote repository.
```
dmitrijostalskij@MacBook-Pro-2 Git % git push -u origin main
Total 0 (delta 0), reused 0 (delta 0)
To github.com:olyacenko/Git.git
   a97c1d1..dc2bf80  main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
dmitrijostalskij@MacBook-Pro-2 Git %  
```
7. In the CheckLists branch create a text document with the Check List structure.
```
dmitrijostalskij@MacBook-Pro-2 Git % git checkout CheckLists
Switched to branch 'CheckLists'
Your branch is up to date with 'origin/CheckLists'.

dmitrijostalskij@MacBook-Pro-2 Git % vim checklist_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % cat checklist_pattern.txt
id: | title: | environment: | precondition: | inputs: | STR: | ER: | AR: | status: | attachment: | bug_link|
------------------------------------------------------------------------------------------------------------
    |        |              |               |         |      |     |     |         |             |         |
dmitrijostalskij@MacBook-Pro-2 Git % 
```
8. Push the Check List structure to the remote repository.
```
dmitrijostalskij@MacBook-Pro-2 Git % git add checklist_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % git commit -m "add file checklist_pattern.txt"
[CheckLists 84160db] add file checklist_pattern.txt
 1 file changed, 3 insertions(+)
 create mode 100644 checklist_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 415 bytes | 415.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:olyacenko/Git.git
   a97c1d1..84160db  CheckLists -> CheckLists
dmitrijostalskij@MacBook-Pro-2 Git % 
```
9. On the remote repository make a Pull Request from CheckLists branch to main.

Go to `Pull requests` => `create a pull request` => in “Compare changes” select branches: `base: main` `compare: checklists` => `create pull request` => `merge pull request` => `confirm merge`
```
Merged olyacenko merged 1 commit into main from CheckLists  1 minutes ago
Pull request successfully merged and closed
```
10. Synchronize remote and Local "main" branches.
```
dmitrijostalskij@MacBook-Pro-2 Git % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

dmitrijostalskij@MacBook-Pro-2 Git % git pull
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), done.
From github.com:olyacenko/Git
   dc2bf80..904b33f  main       -> origin/main
Updating dc2bf80..904b33f
Fast-forward
 checklist_pattern.txt | 3 +++
 1 file changed, 3 insertions(+)
 create mode 100644 checklist_pattern.txt
dmitrijostalskij@MacBook-Pro-2 Git % 
'''
