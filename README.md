//written in main branch

# This repository is just made to teach myself Git.

2-7-24, 2:31pm :    Just learnt:

``` bash
$ git --version
```

``` bash
$ git config --global user.name "chandrima-hazra"
```

``` bash
$ git config --global user.email "*****@gmail.com"
```

``` bash
$ mkdir july-proj
```

``` bash
$ cd july-proj` (C:Users\user\july-proj)
```

Then initialised an empty Git repo in folder july-proj: 
``` bash
$ git init
```

then created a naked intro.html file and checked whether the changes I had made was tracked or not:
``` bash
$ git status
```

and then staged it to the repository and checked whether the changes I had made was tracked or not: 
``` bash
$ git add intro.html
```
``` bash
$ git status
```

Then created this README.md file.

#

2:50pm : Now I've created a crappy-style.css file, to make my intro.html file feel less shameful.

``` bash
$ git add --all
```
OR 
``` bash
$ git add -A
```

This staged both my newly added files into the repository.
#

3:18pm : Made my first commit into the repo. YOU WILL ALWAYS HAVE TO STAGE YOUR COMMITS FIRST!!!
``` bash 
$ git commit -m "here's my first commit"
```

Then made a small change in intro.html file and checked the status.
``` bash
$ git status --short
```

and it showed `M intro.html`, M meaning modified.

so you can even commit changes without writing add command, as I am going to do now:
``` bash
$ git commit -a -m "updated README.md"
```

to view history of all your commits:
``` bash
$ git log
```

created lalala.txt and filled it with rubbish.

``` bash
$ git add -A
```

``` bash
$ git commit -m "updated README.md and created lalala.txt"
```

#

4:00pm : Now I stuffed in some more rubbish in lalala.txt.

``` bash
$ git commit -a -m "updated README.md and stuffed some more rubbish in lalala.txt"
```

I then renamed lalala.txt to rubbish.txt.

``` bash
$ git add --all
```

``` bash
$ git commit -m "updated README.md and created lalala.txt"
```

#

//written in intro-image branch

4:48pm : I created a new branch named intro-image.

``` bash 
$ git branch intro-image
```

``` bash
$ git checkout intro-image
```

Then I added some relatable chess memes in intro.html.

``` bash
$ git add --all
```

``` bash
$ git status --short
```

```A  chess-meme1.png```

```A  chess-meme2.jpeg```

```M  crappy-style.css```

```M  intro.html```

``` bash
$ git commit -m "added some chess memes in intro.html"
```

``` bash 
$ git log
```

`ls` command gives list of all the files present in the current dir.

#

5:32pm : made another branch named "just-remembered-something".

``` bash
$ git checkout -b just-remembered-something
```

``` bash
$ git branch
```

Then I made some changes in intro.html.

``` bash
$ git commit -a -m "not important to know, just too lazy to type a commit message"
```

``` bash
$ git log
```

Then I merged this branch with the main branch.
Before that I need to switch to the main branch.

``` bash
$ git checkout main
```

``` bash
$ git merge just-remembered-something
```

Since both branches were now pointing to the same commit, I deleted the just-remembered-something branch.
``` bash
$ git branch -d just-remembered-something
```

Now, back to intro-image branch, just made some more changes to the intro.html, style.css and README.md files.

``` bash
$ git add -A
```

``` bash
$ git commit -m "added another chess meme in intro.html"
```

``` bash
$ git status
```

As all the changes I had made in intro-image branch seemed fine, I decided to merge this branch with the main branch.

``` bash
$ git checkout main
```

``` bash
$ git merge intro-image
```

This command resulted in a conflict between the 2 branches in intro.html, which, ofcourse, I created on purpose for the sake of learning.
Then I made necessary chanegs in the file of our concern and resolved the conflict.

``` bash
$ git add intro.html
```

``` bash
$ git commit -m "resolved conflicts"
```

``` bash
$ git branch -d intro-image
```

Then I went to GitHub, created this repo, copied the URL and wrote the following command:
``` bash
$ git remote add origin  https://github.com/hazraChandrima/learning-git.git~
```

This means that I want to add my remote repo(in my desktop) with the URL as an origin to my local repo on GitHub.
Now, to check whether this remote origin exists, I write:

``` bash
$ git remote -v
```

```origin  https://github.com/hazraChandrima/learning-git.git~ (fetch)```

```origin  https://github.com/hazraChandrima/learning-git.git~ (push)```

But then I realised that I didn't copy the URL correcctly. So, I removed remote origin.
``` bash
$ git remote remove origin
```

``` bash
$ git remote -v
```
showed nothing, confirming that the remote origin got deleted.

``` bash
$ git remote add origin  https://github.com/hazraChandrima/learning-git.git
```

``` bash
$ git remote -v
```

```origin  https://github.com/hazraChandrima/learning-git.git (fetch)```

```origin  https://github.com/hazraChandrima/learning-git.git (push)```

``` bash
$ git branch -M main
```

``` bash
$ git push -u origin main
```

And I was done.

....pushing my files to the repository.

I edited this README.md file on GitHub, and wanted to update my local Git repo as well.

``` bash
$ git status
```
showed me:

``` bash
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)
nothing to commit, working tree clean.
```

``` bash
$ git fetch origin
```

``` bash
$ git log origin/main
```

``` bash
$ git diff origin/main
```

``` bash
$ git merge origin/main
```

``` bash
$ git status
```

Now, it showed:

``` bash
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean.
```
👍

This can be done in another, much shorter way as well, by using the pull command, which is a combination of fetch and pull command.

``` bash 
$ git diff origin/main
```

``` bash
$ git pull origin
```

## Forking a repository
1. Copy the original repository URL.
2. Fork the repo.
## Cloning a repository
3.
``` bash
$ git clone <original repo URL>
```
## Configuring remotes
4.
``` bash
$ git remote -v
```
we see that the remote origin is set to the original repository. By convention, remote origin must be set to the forked repo, and remote upstream should be set to the original repo. So we rename our remote origin to upstream.
``` bash
$ git remote rename origin upstream
```
5. Copy the URL of our own fork, and set remote origin to our forked repo.
6.
``` bash
$ git add remote origin <forked repo URL>
```
#

That's it for this repo. 😉


thank you.
# 

this line has been written in branch 2.

another line has been added.

this line has been written in branch 3.

this line has been written in branch 4.

this line has been written in branch 5.

this line has been added in branch 6.

this line has been added in branch 7.

this line was wirtten in main branch, just adding a few lines here and in other files as well.

