<div id="top"></div>

<br />
<div align="left">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="images/Github-icon.png" alt="Logo" width="100" height="100">
</a>

<h3 align="center">Version Control Technologies</h3>
  <p align="center">
    GIT
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
    <ol>
        <li><a href="#Getting-Starting">Getting Starting</a></li> 
        <li><a href="#Introduction-to-Local-repository">Introduction to Local repository</a></li> 
        <li><a href="#Notes">Notes</a></li>
  </ol>
</details>




# Introduction to Local repository

1. create new folder as a `Working Directory` for your `own project`
2. use `git init` to create (initialize) local repository on your machine for `this` project<br>
    * each project has only one local repository<br>
    * a hidden .git file will be created<br>
```sh
  git init // in your local project direcotry 
  ```

3. add your project files and put it in `staging Area` by applying `git add` command
    * staging area (index area) tracks any changes in your project file

```sh
  git add <file-name>
  
  ```

* After editing on your file re-type the command

```sh
  git add <file-name>
  git add . // update all files to staging area 
  ```

4. to save your changes by applying `git commit` and put a message, so you can read it later and understand the changes
   through it.<br>
   * create id for each commit
```sh
  git commit -m "commit_message"
  ```

5. push your project from local repository to remote repository
    - first time for repository creation
        - origin is alias for https link
6- added my ismail
```sh
git branch -M main
git remote add origin 'URL'
git push -u origin main
  ```

<p align="right">(<a href="#top">back to top</a>)</p>



# Notes
1. `git remote -v` **will tell you what repo is connected your working directory**
```sh
git remote -v
  ```

2. `git status` to see the status of all created files in project directory
```sh
git status
```

3. `git branch` will tell you name of the branch you're currently in
```sh
git branch
```

4. `.gitignore` files in this file you put all not wanted files to stop it form getting pushed to the repository
```sh
git branch
```

5. `-u` is standing for `--set-upstream` 
```sh
git push -u origin master
git push --set-upstream origin master
```

6. `git log` **give you all commits on your project history**<br>
    * commit ID<br>
    * Author<br>
    * Date<br>
    * message added when commit happened <br>
    * `git log -p` shows more details on each commit<br>
```sh
git log
  ```

7. `git restore --staged` **Removes the file from the Staging Area, but leaves its actual modifications in working directory untouched**)
   * file will not be added in history
```sh
 git restore --staged <file-name>
```

8. `git rm --cached` **removes a file from the staging area. The files from the working directory will remain intact**<br>
    * will add the removed file in history
    * for example:<br>
        * you have 5 files in working directory <br>
        * only 3 of them are ready for being committed<br>
        * apply this line to remove the 2-unready files from staging area<br>
        * then commit the 3-ready files<br>
```sh
  git rm --cached <file-name>
  ```
9. understanding `git restore` <br>
* file added in staging area  (have 1 line)
* modified file in `working dir` (have 2 lines)
* want to go back to the file before new modifications use `git restore`
```sh
  git restore <file-name>
 ```
<p align="right">(<a href="#top">back to top</a>)</p>




# Branching:
master branch is the best version of your project (can be connected to server)


when creating a branch, do it from master branch 
## merging 

create new branch and go to it 
```html
git checkout -b <new-branch-name>   // method1
git switch -C <new-branch-name>     // method2
git switch <branch-name>   // switch between branches
```

merge 2 branches in local machine first apply
```html
git switch <branch-name>
```
then merge it with the desired branch
```html
git merge <branch-name>
```

to show all commits with which branches 
```html
git log
```
show all branches in local and remote
```html
git branch -a 
```

`git fetch --all` get all untracked commits in remote, and you can see all of them <br>
once you have chosen one to edit it<br>
this branch is on local and up to date<br> 
but if you already have it on your machine locally you will be required to `pull` the new changes (new commits)
by applying `git pull` on this branch.
```html
git fetch --all
```
**So the Difference between `git pull` and `fetch all` is that:<br>**
* `git fetch all` allows to only see changes without taking it to locally
* `git pull` git pull = fetch  --all + all merge

to delete branch
```html
git branch -D <branch-name>
```

to rename branch
```html
git branch -M <new-name>
```

# Difference between Rebasing and merging 

## Merge:
used to update the `master branch` with the added commits that a feature has.<br>
when a feature require new commits from the main branch a merge process will be required from the main to the feature
as the number of  the required commits in the feature branch increases more merge processes are required with additional commits
that causes the history of the commits in the feature branch messy and untraceable<br>
```html
git checkout <feature-branch>
```

## Rebase:
it's in its simplest definition the reassigning process of the `base of the branch` rather than merge the commits of the main branch
`simply rebase the branch` to the `commit` that has features that serves your need in the branch<br>
```html
git rebase <branch that has the required commits>
```


# Difference between reset , reset --hard and revert

## git revert 
running that command puts the branch in the selected commit followed by a commit saving that revert
in the history of the branch log
```html
git revert <commit to return-to id>
```

## git reset
cancel that commit without deleting the added files or canceling the added modifications that added in the commit
the reset process is not saved in the log of the branch

```html
git reset < commit that needed to canceled id>
```
## git reset --hard
cancel that commit and delete any new files added in that commit and cancel any modifications in the files added in that commit
the reset process is not saved in the log of the branch

```html
git reset --hard <commit that needed to cancled id>
```
