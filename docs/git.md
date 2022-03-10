
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
### Add all files and commit 
```sh
git commit -am 'commit message'
```
This does not work with new files, which requires the capitalized -A flag
```sh 
git commit -A
git commit -m 'commit message'
```
