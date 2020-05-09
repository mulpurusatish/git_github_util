### Create Local Repository ###
mulpu@satishvm MINGW64 ~/github/projects/git_commands
$ git init
Initialized empty Git repository in C:/Users/mulpu/github/projects/git_commands/.git/

### ADD file ###
mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ touch first.txt

### Verify the STATUS ###
mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        first.txt

nothing added to commit but untracked files present (use "git add" to track)

### Add file to the STAGING area / environment ###
mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git add first.txt

mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   first.txt
		

Note : Staging environment ie stage / index

###  Create COMMIT ###

mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git commit -m "first.txt : First commit"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

Note : GIT is getting used for the first time, please set the required info - name & email.

mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git commit -m "first.txt : First commit"
[master (root-commit) 0f7d73b] first.txt : First commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 first.txt

### Create a new BRANCH ###

Plannig to add new FEATURE, but worried about the consequences. This is where GIT BRANCHES come in. 

Branches allow you to move back and forth between 'states' of a project. Once you're done with the feature / page, you can merge your changes from your branch into the master branch.

mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git branch
* master

Checkout option will be used to create new BRANCH n switched to the new BRANCH with the MASTER branch code, here.

mulpu@satishvm MINGW64 ~/github/projects/git_commands (master)
$ git checkout -b branch1                                                                                               
Switched to a new branch 'branch1'

mulpu@satishvm MINGW64 ~/github/projects/git_commands (branch1)
$ git branch
* branch1
  master
  
Now we can have the changes in the respective branches only.. until MERGE happens.  


###  Create Repository on GitHub ###
Till now, we have the CODE in local repository only. Suppose if required to work with the team, GitHub Repository is the place where we can store the CODE.

Create a Repository.'git_github_util', in GitHub. Follow the below steps to PUSH the changes from LOCAL to GitHub Repository.

mulpu@satishvm MINGW64 ~/github/projects/git_commands (branch1)
$ git remote add origin https://github.com/mulpurusatish/git_github_util.git

mulpu@satishvm MINGW64 ~/github/projects/git_commands (branch1)
$ git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 224 bytes | 44.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/mulpurusatish/git_github_util.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.


### PUSH a BRANCH to GitHub ###

   touch README.md
   git add *
   git status
   git commit -m "README.md added"
   git status
   git push origin branch1
   
   mulpu@satishvm MINGW64 ~/github/projects/git_commands (branch1)
$ git push origin branch1
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.51 KiB | 258.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To https://github.com/mulpurusatish/git_github_util.git
   0f7d73b..ea7c02b  branch1 -> branch1
   
   

### Create a PULL Request ###

PULL request will be used to ALERT the Repository Owner's that you want to make some changes to their CODE.

PULL request will MERGE the changes from CHILD --> MASTER


### REVERT the changes, if required ###
REVERT / Undoing the COMMIT by using the HASH code

###  Bring the changes from GitHub to Local Repo ###

git pull origin master

Pulling the changes from the Origin / GitHub Master branch to your local MASTER branch
		

