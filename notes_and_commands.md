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
``` sh 
$git add . 
```
+ **or** there's another option:
``` sh $git checkout <filename>```
+ what **checkout** does is reverts any changes that you made back to the state that it was in at the time of the last add (not the last commit, the last **add**, the last time it went to the staging area, commit or not)
+ this saves you from having to go back and erase a ton o' crap if you decide that you just want to revert to the previous state.
+ _Convenient!_
+ here is a similar, yet different, command:
``` sh 
$ git reset HEAD <filename> 
```
+ what this does is reset what's been committed to your working environment.
+ so the both change what's in your local repo, but:
  - **_checkout <filename>_** changes what **hasn't** been committed
  - **_reset HEAD <filename>_** changes what **has** been committed
+ note that my understanding is very, very limited here....
+ there is also a way to checkout the hash that you get when you run a log and create another branch... I don't understand that at all

#### Deleting files
+ to delete a file, first get rid of it in your local repo folder by a simple deletion
+ after that, run a **_$ git status_** and the file will show up as being deleted from the local repo -- this doesn't mean that it's been deleted from the remote repo, though
+ you have some options, now:
  - to _undelete_, that is, move the file from your the trash back into the local repo, run the checkout command on the file:
  ``` sh
  $ git checkout <filename>
  ```
  - to _really_ delete it, you need to push it through, that is:
  ``` sh
  # delete the file from your local repo
  $ git add <filename>  # for a single file, or
  $ git add .           # if your are deleting a bunch of stuff
  $ git commit -m "just deleted some files"
  ```
  - if you deleted a file, then added it, but _then_ decide you want to keep it, you can unstage it using _reset_:
  ``` sh
  # delete the file
  $ git add <filename>
  $ git reset HEAD <filename>
  $ git status
  $ git checkout <filename>
  ```
  - you can combine the steps of manually deleting the file and adding the removal to the staging area by using the linux command _remove_:
  ``` sh
  $ git rm <filename>
  ```
  - then if you check the status, you'll see that the _add_ command has been done, too, nothing to do but _commit_
  -  finally, let's say that you have deleted a bunch of stuff and you've done some other stuff, too, you can just use the double flag _all_:
  ``` sh
  git add --all
  ```
  - this will put everything into the staging area, where all you have left to do is commit




http://www.lynda.com/Git-tutorials/Initializing-adding-committing-status/409275/416547-4.html
