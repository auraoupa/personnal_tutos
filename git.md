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
  * git remote show origin
  
## Branching

  * git branch testing
  * git log (tells you on which branch you are)
  * git checkout testing
  * git checkout master
  * git merge testing (with the current branch master)
  * git branch -d testing (delete the branch)
  

## Removing definitively a file
  * git filter-branch --force --index-filter \ 'git rm --cached --ignore-unmatch report2-2017-05/Misc/2017-05-30-AA-differences-between-Mercator-and-Drakkar-settings-for-ORCA12.pdf'
  * git push origin --force --all
  
  
## Contribute to another person's repo

  * git checkout -b new_branch
  * les modifs
  * git commit -am "comment"
  * git push origin new_branch
  * sur github cliquer sur open pull request
  
## Diff

  * après un git pull : git diff HEAD pour voir les diffs entre le depot distant et le master local
  * git diff --staged
