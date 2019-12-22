# demo
Demo of using GitHub

### When you create a branch test_branch locally, make some changes on this new branch. Then you need create test_branch remotely and push the changes remotely

  git push --set-upstream origin test_branch  
  
  or 
  
  git push -u origin test_branch
  
### List local and remote branches
  
  git branch -a                           
  
  git checkout master
  
  git merge test_branch
  
### Remove branch locally
  
  git  branch -d test_branch    
  
### remove branch remotelly
  
  git push origin --delete test_branch   

### rename branch
  
  git branch -m old_name new_name
