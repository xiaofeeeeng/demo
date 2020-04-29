# demo
Demo of using GitHub


---
## Global setting

`git config --global user.name 'myname'`

`git config --global user.email 'myname@example.com'`


**switch between different GitHub account when making commits**

`git config user.name 'account1'`

`git config user.email 'account1@example.com'`

'*commit changes*'

`git push origin master`

`git config user.name 'account2'`

`git config user.email 'account2@example.com'`

'*commit changes*'

`git push origin master`

---
## Connect local and remote

### Method 1

***Create a remote repository on GitHub first, then copy with HTTPS***

`git clone copiedHTTPS`

### Method 2

`mkdir Test`

`cd Test`

`git init`

'*commit changes*'

'*Create a remote repository Test on GitHub, then copy with HTTPS*'

`git remote add origin copiedHTTPS`

'*If the repository is being forked, then you should do the following*'

`git remote add upstram originalrepositoryHTTPS`

***if there is error like fatal: refusing to merge unrelated histories, you should do***

`git pull origin master`

`git pull --allow-unrelated-histories`

***(then follow the hints)***

---
## Deal with regrets

### Regret before git add

***Method 1***

`git stash`  (*store all the local changes*)

`git stash drop` (*this will discard all the local changes*)

***Method 2***

`git checkout .` (*this will discard all the local changes on all files*)

`git checkout filename` (*this will discard all the local changes for filename*)

***Method 3***

`git reset --hard` (*this will discard all the local changes on all files*)

### Regret after git add

`git reset HEAD`

### Regret after git commit

`git reset HEAD~1`  (*this will keep all the local changes*, Do Not put space between HEAD and ~)

### Regret commit or message

`git rebase HEAD~3 -i`   (*display the lastest 3 commits*)


---
## Branch

### When you create a branch test_branch locally, make some changes on this new branch. Then you need create test_branch remotely and push the changes remotely

  `git push --set-upstream origin test_branch`
  
  or 
  
  `git push -u origin test_branch` (This is much easier compared with the previous one.)
  
### List local and remote branches
  
  `git branch -a`                           
  
  `git checkout master`
  
  `git merge test_branch`
  
  `git branch --merged`     (*Use this command to see the merged branch before you delete branch*)
  
### Remove branch locally
  
  `git  branch -d test_branch`    
  
### remove branch remotelly
  
  `git push origin --delete test_branch` 
  
  or 
  
  `git push origin -d test_branch`

### rename branch
  
  `git branch -m old_name new_name`
  

---
## Gitignore


---
## SSH


---
## Tag


---
## alias of the command history 
`alias graph=“git log —-all —-decorate —-oneline —-graph”`


---
## git log
`git log -p` (show detailed changes)

`git log -4` (show 4 log messages)

`git log -2 —-pretty=oneline`  (only display commit messages)

`git log —-pretty=medium`   (default)

`git log --pretty=fuller`



