
# Git Cheatsheet

[My notes](https://rcmadden.github.io/notes/#/git-version-control) of basic commands for getting re-started using git from [Udacity’s Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123) free course completed 2/2021, the [Atlasian Tutorial](https://www.atlassian.com/git/tutorials), [Git Documentation](https://git-scm.com/docs) plus random notes I have stashed in several locations from previous experience.

## Creating a Repo
### Empty Directory
Initialize an empty Git repository in the current directory
```bash 
git init
```
Setup a remote repo on github or bitbucket
```bash 
git remote add <remote_name> <remote_repo_url>
git push -u <remote_name> <local_branch_name>
```
Example:
```bash 
git push -u origin main
```
### Existing Directory with Files
```bash 
cd /path/to/my/code
git init   #(1)
git add .  #(2)
git commit #(3)
```
1.  Inside code directory initialize a /path/to/my/code/**.git directory**.
2.  Add all existing files to the index.
3.  Record the pristine state as the first commit in the history.

### Clone Existing Repo
```bash
git clone <repo>
git fetch # will update all the remote-tracking branches
git pull # will in addition merge the remote master branch into the current master branch
```
### Add and Commit All (single command) 
```sh
git commit -am 'commit message'
```
This does not work with new files, which requires the capitalized -A flag
```sh 
git commit -A
git commit -m 'commit message'
```

### Edit Last Commit Message
```
git commit --amend
```
In the text editor, edit the message and close the file.

## Branching

### List Branches
list all branches in local and remote repositories:
``` 
git branch -a 
```
list remote branches:
``` 
git branch -r
```
lsit branches and their commits:
``` 
git show-branch
```


### Switching Unstagged Changes to a New Branch
``` 
git switch -c new-branch-name
```

### Delete Branch
Move to different branch
#### Delete Local Branch
``` 
git branch --delete branch-name
```
#### Delete Remote Branch
```git push origin -d branch-name
```
where "orign" is the remote-name


### .gitignore

[Add .DS_Store in all sub-directories to .gitignore](https://gist.github.com/rcmadden/ed57a253474c833eba01f7eaca6ec374#file-add-ds_store-into-gitignore-for-the-sub-directory-md)
```
**/.DS_Store
```

## Issues and Errors
### git push says "everything up-to-date" even though I have local changes

git push origin master

And it shows the message Everything up-to-date.

to fix this this issue, try these steps

```
git add .
git commit -m "Bug Fixed"
git push -u origin master
```
source: [Stack Overflow](https://stackoverflow.com/questions/999907/git-push-says-everything-up-to-date-even-though-i-have-local-changes 
)
