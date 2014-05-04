Git Quick Reference
===================
This is my first Git project.  I will use it to learn a little bit about git. A git bit is what I will learn by using this project.

todo: convert to markdown format.  see the following resources for markdown
* [introduction to markdown](http://daringfireball.net/projects/markdown)
* [using markdown in rstudio](http://www.rstudio.com/ide/docs/authoring/using_markdown)

So far I've learned about the following commands

## getting started
git init  # create local repository  
git config  
git config --list  
git add . # add all new files  
git add -u # updates tracking for files that changed names or were deleted  
git add -A # does both of the previous  
git rm <file> # remove a file  
git rm --cached <file> # unstages the file without deleting it  
git status  
git diff  # displays changes in working dir but not staged  
git diff --cached # displays changes that are staged (and will go into next commit)  
git commit  
git commit -m "update description"  
git commit -a  # commit all tracked files  
git log # display list of commits  
git log --oneline  # display brief list of commits  
git config --global alias.one 'log --oneline'  # create the command alias "git one" for "git log --oneline"  
  
## remote servers  
git remote # list remote servers (short names only)  
git remote -v # verbose list remote repositories (show urls)  
git remote add <short name> <url>   
git remote add origin https://github.com/<username>/<repo name>.git # link local repo to github  
  
## push/pull  
git clone <url> # create local master  
git fetch # retrieve remote project but don't merge  
git pull  # retrieve branch and merge  
git push <remote server> <branch> #  
  
## tags  
git tag # list tags  
git tag -n # list tags + messages  
git tag -l 'v1.*' # search for tags matching  
git tag -a <tag> -m "<tag description>" # create tag  
git show <tag> # show tag data and associated commit  
git tag <tag> # create a lightweight tag  
git tag -a <tag> -m "<tag descr>" <commit checksum starts-with>  
git tag <tag> <tag> -f -a # edit tag message using editor  
git push origin <tag> # share specific tag with remote  
git push origin --tags # share all tags with remote  
  
## branches  
git checkout -b <branch name> # create a new branch (copy of master)  
git branch # list branches with current branch starred  
git checkout master # make 'master' the current branch  

## under the hood
git ls-file --stage # list files in the index (i.e. staged)  
git cat-file <file hash>  
