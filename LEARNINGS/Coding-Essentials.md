
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

Source - 1
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

Source -2 
The following commands in the vs code terminal to push changes to master origin.

	git status	
	git pull	
	git status	
	git add .	
	git commit -m "leave a message here"	
	git push 	
		
		
VScode to push changes		
	check changes	in source control
	Stage changes	click '+' on changes in source control
	Add message	
	Click commit (tick mark) 	
	Sync & push	(or pull then push)

## Merge Conflict

Source- 1
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


Source - 2

Create Merge conflict

When same file changes in github, vscode on same line is made.
Scenario: github change commit, vscode commit then push

merge conflict code flow:
Accept current change or Incoming change or accept both
git add .
git commit -m " "
git merge
git pull
git push



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




## Github Universe: Codespaces - Git coding fast

General software coding steps:
* checkout code
* download dependencies
* Fighting dependecies conflicts
* installing tools
* debugging bad interactions with other tools
* switching branches
* constant maintenance of our developer environments

Codespaces solve above problems, need not to worry about them.

We get clean isolated pre configured environment with the power of configures code.

Codespaces automates environment setup, it hands you a fully built and ready machine that is exactly same every time in seconds.

Instead of comparing production to all the machines with different different setups, you only have to compare them to one at any point in got history.

It works on every machine, evry tool, everyone.

When we click code spaces, a developer environment spins up in cloud pre-installed with "universal image". It has a common set of tools and runtimes like python, node, docker, ml etc libraries. Github maintains the image so that we dont have to keep up with latest tooling and security patches.

Its a clean environment, doesn't even recognize git, just like local. Codespaces also loads dot files automatically so that your favourite tools stay with you.							

Cli provides incredible access to remote machine in the way that works for you and ability to automate common scripts, full access to the code spaces API. Codespaces allows to switch seamlessly with your browser in whatever device you wish to work on.							

Npm run dev is running automatically and the core and core files are opening files. Its just config as code right next to your project.							

We specify minimum post requirements, the build, the file that should open on launch and which processes to start in which port to forward. 							

When we vscode from browser to local vscode editor, this will reload local vscode and connect directly to that code space. Even though it is local, vscode connects to remote codespaces of github. Keep sync settings browser on.

You can upgrade development environment through codespaces very quickly by allotting memory and ram. Codespaces are secure by default and they're private by default. But you can make public or private or oraganization. This make it easy for developers to collaborate and work. We can live share too.		

Git hub cli is automatically installed in universal image, we can create PR directly from command line so that we don't need to break our code flow.							

It is easy to have dev container in codespaces.

Learn to use co-pilot in vscode.

Learn about pull requests, github pull request extension in vscode.