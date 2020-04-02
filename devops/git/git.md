# Work with Git :

* **What is it ?**
Git/Github is a versioning management software to work on your projects.
Github is a software development platform for Git and collaborative work.

* **Git set up:**
```git config --global user.name <your_name>```
```git config --global user.email <your_email>```
```git config --global user.color-ui true/false```
```git config --list```  (q -> to quit)


* **Create Repository:**

[Local]
```mkdir <folder>``` : to create your folder repo
```cd folder``` : to access it
```ls``` : to list all the elements present in the folder
```git init``` : transform your folder in git project
```git diff``` : show modifications done on files

[Remote]

```Access https://gist.github.com/username``` to create a repository

* **Basic commands:**

```git status``` : to access the pending modifications
```git clone <REPO_URL>``` : to copy an existing repo
```git add [file(s) | . | * | a | *.html]``` : to add a file to the staging area
```git commit -m "<your_message>"``` : to commit your modifications to your repo
```git commit --amend "<with_modified_text>"``` : to amend a previous commit
```git branch <BRANCHNAME>"``` : to create a new branch
```git checkout -b <BRANCHNAME>``` : to create a new branch and access it
```git checkout``` : to access a previous commit and change branch
```git revert / reset``` : to cancel or move back to previous commits
```git log``` : show the last commit

* **Commands for distant repository:**

```git remote add upstream <distant_repo_url>``` : to add a distant repo to your local project
```git pull upstream <BRANCHNAME>``` : update your local repo with a distant repo.
```git pull origin <BRANCHNAME>``` : update your local repo with your remote one
```git pull <REMOTENAME> <BRANCHNAME>``` : update changing from a remote.
```git push``` : send your local modifications to the distant repo
```git remote -v``` : show the URL remote
```git remote set-url <REMOTENAME> <URL>``` : to change a remote URL
```git merge <BRANCHNAME> | git merge origin <BRANCHNAME>```  : to merge a branch locally | to a distant repo


