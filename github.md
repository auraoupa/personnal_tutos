# Outil github #

  * purpose : keep tracks of changes on scripts, produce web pages, online storage of scripts

## Basic commands ##

Using it at work :

    git config --global http.proxy  https://www-cache.ujf-grenoble.fr:3128

When you want to make a local copy of a online repository :

    git clone https://etc...

When you want to add modifications to a repository, locally :

    git add .
    git commit -m "bla bla"
    git push
 
When you want your local repository to be updated :

    git pull

When you want to get rid of a file :

    git rm
    
## Synchronise a local repo with github

 * initialise with git init, git add., git commit ... locally
 * create a repo on github
 
         git remote add origin https://github.com/auraoupa/CMEMS.git 
         git pull origin master 
         git push origin master
         
 * when the remote name has changed
       
          git remote set-url origin https://github.com/auraoupa/CMEMS-notebooks.git
    
     
## Other stuff ##

When you want to produce a personal web page :

    create a repository yourname.github.io
    put some html in it, with at least an index.html
    see your web page at http://yourname.github.io
 
When you want to produce another web page :

    create a repository repo
    create a branch gh-pages
    make the branch gh-pages the default branch (in settings/branches)
    put some html in the gh-pages branch
    see your web page at http://yourname.github.io/repo


## Authorization for private repositories

 https://education.github.com/discount_requests/new

## Download a single file from github

curl -O https://raw.githubusercontent.com/lesommer/notebooks/master/path/to/notebook.ipynb => marche pas ...
