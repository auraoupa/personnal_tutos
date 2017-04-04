# How to use git

## Transform a repository into a git rep

  * git init
  * git add .
  * git commit -m "comments"
  * git status 
  * git log
  
## Cloning an existing repository

  * git clone https://github.com/auraoupa/personnal_tutos.git
  * git fetch
  * git merge
  * git pull = fetch + merge
  * git push
  
## Synchronise a local rep on github

  * create a rep on github examples.git
  * git remote add origin https://github.com/auraoupa/examples.git 
  * git pull origin master 
  * git push origin master
  
## Branching

  * git branch testing
  * git log (tells you on which branch you are)
  * git checkout testing
  * git checkout master
  * git merge testing (with the current branch master)
  * git branch -d testing (delete the branch)
  
