##Lynda tutorial:  Up and running with Git and GitHub
####Setting up a local repo
+ create the folder that you want for the local repo, then run this command:
``` sh $ git init ```
+ next, create whatever content you want to add.  
+ recall that there are three areas in your entire git project:
   - the local repo:  that's your folder on your computer
   - the staging area:  that's where you add to and commit from
   - the remote repo: that's where other people can access
+ next, add the files to the staging area with one of these commands:
``` sh
$ git add .     # adds all files that have recently changed in local repo
$ git add <filename> # for specific files 
```
+ you can see the status of your files using this command:
``` sh $ git status ```
+ you can see a log of your commits with this command:
``` sh $ git log ```
+ if you get a message that says something like **_please tell us who you are_**, you need to run the commands that tell git... well, who you are:
``` sh
$ git config --global user.email "you@example.com"
$ git config --gloabl user.name "Your Name"
```
+ I always get these confused, as the syntax is confusing, but I think an actual example of this would be:
``` sh
$ git config --global "bill_hicks@uic.edu"
$ git config --global "Bill Hicks"
```
+ but I could be wrong

####Working with the staging environment
+ once we have made some changes to our files, and we want to add them to the staging area, we can do this:
``` sh $git add . ```
+ **or** there's another option:
``` sh $git checkout <filename>```
+ what **checkout** does is reverts any changes that you made back to the state that it was in at the time of the last add (not the last commit, the last **add**, the last time it went to the staging area, commit or not)
+ this saves you from having to go back and erase a ton o' crap if you decide that you just want to revert to the previous state.
+ _Convenient!_
+ here is a similar, yet different, command:
``` sh $ git reset HEAD <filename> ```
+ what this does is reset what's been committed to your working environment.
+ so the both change what's in your local repo, but:
  - **_checkout <filename>_** changes what **hasn't** been committed
  - **_reset HEAD <filename>_** changes what **has** been committed
+ note that my understanding is very, very limited here....



http://www.lynda.com/Git-tutorials/Initializing-adding-committing-status/409275/416547-4.html
