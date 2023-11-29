# cherry-pick

```BASH
nikky@nikky:/$ touch index.html

nikky@nikky:/$ git init

Initialized empty Git repository in /home/nikky/Desktop/YourFile/girTest/.git/

nikky@nikky:/$ git add .

nikky@nikky:/$ git commit -m "fresh repo"
[master (root-commit) 9dca4e6] fresh repo
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html

nikky@nikky:/$ git branch secondBranch

nikky@nikky:/$ git checkout secondBranch

Switched to branch 'secondBranch'

nikky@nikky:/$ touch main.css

nikky@nikky:/$ git add .

nikky@nikky:/$ git commit -m "css file add"
[secondBranch df35b4b] css file add
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 main.css

nikky@nikky:/$ git checkout

nikky@nikky:/$ git checkout master
Switched to branch 'master'

nikky@nikky:/$ git log secondBranch --oneline 
df35b4b (secondBranch) css file add
9dca4e6 (HEAD -> master) fresh repo

nikky@nikky:/$ git cherry-pick df35b4b
[master 57474d7] css file add
 Date: Wed Nov 29 04:27:27 2023 +0600
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 main.css

nikky@nikky:/$ git checkout

nikky@nikky:/$ git checkout secondBranch
Switched to branch 'secondBranch'

nikky@nikky:/$ echo "secondBranch branch say hellow" > main.css

nikky@nikky:/$ git add .

nikky@nikky:/$ git commit -m "first text"
[secondBranch 6344d1e] first text
 1 file changed, 1 insertion(+)

nikky@nikky:/$ git checkout master 
Switched to branch 'master'

nikky@nikky:/$ git log secondBranch --oneline 
6344d1e (secondBranch) first text
df35b4b css file add
9dca4e6 fresh repo

nikky@nikky:/$ git cherry-pick 6344d1e
[master a519d4a] first text
 Date: Wed Nov 29 04:29:52 2023 +0600
 1 file changed, 1 insertion(+)

nikky@nikky:/$ git branch 
* master
  secondBranch
```
