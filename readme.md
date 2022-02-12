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
74el el file w m4 7y7oto fel histry
 git restore --staged <file-name>

 restore it from tracked to untrackd 
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




<p align="right">(<a href="#top">back to top</a>)</p>



### config



create folder named master when applying `git init`

file added in staging area (file contains only `1 line of code`)
then the file was modified in working directory (file contains only `2 line of code`)

remove file from staging area and make it `untracked file`

```sh
  git restore <file-name>
  file added in staging area 
  modified in the same file  in working directory
  staging area have 1 line 
  working dir have 2 lines 
  will make it 1 
  working dir updateed bezabt zy el staging area 
  ```





########################################

# Remote repository

there are many tools `GitHub` , `gitlab` , `bitbucket`

https mode will require  `username - password`

ssh public key of my machine and on GitHub trust this machine

`git pull` to get modified files on your project

