# demo
Demo of using GitHub

master branch locally, then create a branch test_branch locally, make some changes on this new branch.

  git push --set-upstream origin test_branch
  
This will also create a test_branch remotely.

  git branch -a                           'list local and remote branches
  
  git checkout master
  
  git merge test_branch
  
  git  branch -d test_branch              'this will remove branch locally
  
  git push origin --delete test_branch    'this will remove branch remotelly


