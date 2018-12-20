# How to use git

astuce générale : git status donne de bonnes indications de ce qu'il faut faire

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
  * pour merger les chosees lineairement, utiliser rebase :
     * on merge une premiere branche dans master
     * on se place sur l'autre branche
     * git rebase master
     * resoudre les conflits si il y a puis git add et git rebase --continue
     * retourner sur master et merger la branche qui est en fast-forward maintenant

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
  * par defaut un diff est entre le workspace et l'index (là où vont les add), si HEAD entre workdspace et local repository
  * après un git pull : git diff HEAD pour voir les diffs entre le depot distant et le master local
  * git diff --staged
  * git diff branch1 branch2
  
## Log

  * git log
  * git log --author=bob
  * git log --pretty=oneline
  * git log --graph --oneline --decorate --all
  * git log --name-status
  * dans .gitconfig [alias] lo = log --graph --all --decorate --date-order pour un beau git log

## Version
  * git checkout bb92e :  pour revenir à un état précédent
  * git reset HEAD^(ou nom d'une version) :  abandonner des modifs commitées pas pushées
  * git revert bb92e : abandonner modifs commitées et pushées => c'est un nouveau commit
  
## Faire un pull d'un depot distant
  * git pull
  * si conflit d'abord git fetch puis git merge origin/master ?
  * si en local j'ai developpé dans une branche et que je veux mettre à jour le depot distant : git rebase origin/master  
  
## Mettre de coté des modifs pour un moment
  * git stash
  * git stash apply/pop cf https://git-scm.com/docs/git-stash

## On peut pusher vers différents repertoires git

## Resolution d'un conflit
  * au cours d'un pull ou merge de branche soit 
      * auto-merge et c'est ok
      * CONFLICT Automatic merge failed alors 
        * les diffs sont reportées dans le fichier incriminé
        * on doit ouvrir le fichier et le modifier en fonction de ce qu'on veut garder comme modifs
        * git add + git commit finalise le merge
      
## Formation
  * https://doc.cc.in2p3.fr/developpements:formation:git
  * https://onlywei.github.io/explain-git-with-d3/
  * https://try.github.io
  * https://learngitbranching.js.org/
