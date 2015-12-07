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
$ git add filename # for specific files 
```
+ you can see the status of your files using this command:
``` sh $ git status ```
+ you can see a log of your commits with this command:
``` sh $ git log ```
+ if you get a message that says something like **_ please tell us who you are_**, you need to run the commands that tell git... well, who you are:
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



http://www.lynda.com/Git-tutorials/Initializing-adding-committing-status/409275/416547-4.html
