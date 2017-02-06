# Outil github #

* purpose : keep tracks of changes on scripts, produce web pages, online storage of scripts

## Basic commands ##

Using it at work :

    git config --global http.proxy  https://www-cache.ujf-grenoble.fr:3128

When you want to make a local copy of a online repository :
 * git clone https://etc...

When you want to add modifications to a repository, locally :
 * git add .
 * git commit -m "bla bla"
 * git push
 
When you want your local repository to be updated :
 * git pull

When you want to get rid of a file :
 * git rm
 
## Other stuff ##

When you want to produce a personal web page :
 * create a repository yourname.github.io
 * put some html in it, with at least an index.html
 * see your web page at http://yourname.github.io
 
When you want to produce another web page :
 * create a repository repo
 * create a branch gh-pages
 * make the branch gh-pages the default branch (in settings/branches)
 * put some html in the gh-pages branch
 * see your web page at http://yourname.github.io/repo
