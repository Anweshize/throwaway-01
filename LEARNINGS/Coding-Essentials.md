
Today's world - Python, Java, Javascript



## Git & Github

* There will be no issues until two different people make updates, until there is merge conflict.
* We can make many commits and push at once.
* Hundreds of developers can work on same things at once in git and git hub.
* In git we can go back at any instance and see the commits made. Its like git remembers the code history.
* Every successful commit gets a unique ID.
* Git page - extension is `.md`



## VS Code Commands

* crtl + R  for recent folders
* crtl + t 
* crtl + p for pages
* Crtl+J for terminal
* crtl+P - select file with name
* vscode editor search - '#' for links.	
* Linking - [#](https......)


## VS Code Commit-Pull-Push

* commands flow for commit: (set path in terminal)
* git status
* git add .
* git commit -m " "    - merge is also a commit
* git status
* git pull
* git fetch     - we are checking whether there is nothing to commit here.
* git push
* git status
* git diff      - to see changes
* git log -m    - no of logs, commits to previous m number

* git config pull ff only - if error is fast forward not possible 

## Merge Conflict

Green - local part

Blue - remote part(github)    - always chose this else we can chose accept both

fetch    - repo, file stays near local but won't show

merge    - files come to local. without fetch, git status won't know that remote is changed.

merge conflicts happens here

git merge --abort        - to abort merge

accept incoming	: if remote is correct

accept combination	: if manual is correct

untracked files - git doesn't know

When git unable to merge make stash.

stash - give name: stash keeps all changes in seperate place.

do git pull before merge.

path has to be correct for files to be in right place when we commit


## Repository

Create repo: New repository - name(anwesh practice) - private - add a file(read me) - save

Clone repo from github: vscode - clone github repo - select a github repo we want to add to vscode - add to local folder (users-Anwesh-repo)

## General
go main repository - press dot(full stop) - takes you to online code editor(vscode mostly) with no terminal.

crtl+enter for updating

branch doesn't effect your main repo

codespaces - virtual machine running behind, have terminal

advantage is all softwares are ready and installed, even java etc

Even if we create something here, it will save as copy

