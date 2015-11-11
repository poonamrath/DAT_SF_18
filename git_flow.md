
# Git Flow

Every day in class, we are going to be interacting with git - and if you do things out of order, it can be very frustrating so let's make sure we have the right flow

--------
##### Starting From Scratch (steps below, followed by code)
* Fork the Class Repo (on github) 
		![Alt text](https://liftopia.box.com/shared/static/9uf1pi1jt41zvbyx80ij2oc9i34syf13.png "Optional title")
* Clone your repo
* Add the instructor remote
* Check Status


```sh
$ git clone https://github.com/[YOUR_USER_NAME]/DAT_SF_18   
$ git remote add instructor https://github.com/ga-students/DAT_SF_18
$ git status
```
----------
##### Typical Pre/In-Class Flow

* Check Status
* add  (stage) any changed files before commiting 
* commit - WITH A MESSAGE!
* Push the files to your personal repo (origin master)
* Check for a clean status
* Pull the new files from the instructor repor

```sh
$ git status    
$ git add folder1/file1.ipynb
$ git add folder2/file2.csv
$ git commit -m "I'm cleaning up my repo before class"
$ git push origin master
$ git status
$ git pull instructor master
```


____________
##### Common Errors
* Forgetting to add a commit message - this will cause a text editor called VIM to open. It should look somethign like the image below. To solve this, enter a message using VIM ([good instructions here](http://stackoverflow.com/questions/13507430/git-commit-in-terminal-opens-vim-but-cant-get-back-to-terminal)). 

    ![Alt text](http://i.stack.imgur.com/d4bbf.png "Optional title")
    

* You see a message about a .swp file. The image looks something like the image below. This is caused by exiting the terminal in the middle of a commit. To solve this, you need to delete the .swp file, [following instructions here](http://stackoverflow.com/questions/13361729/found-a-swap-file-by-the-name).:
    ![Alt text](http://i.stack.imgur.com/wIZ30.png "Optional title")









