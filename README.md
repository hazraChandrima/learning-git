//written in main branch

This repository is just made to teach myself Git.

2-7-24,2:31pm : Just learnt:
$ git --version
$ git config --global usesr.name "chandrima-hazra"
$ git config --global user.email "hazrachandrima6@gmail.com"
$ mkdir july-proj 
$ cd july-proj (C:Users\user\july-proj)

Then initialised an empty Git repo in folder july-proj:
$ git init 
then created a naked intro.html file and checked whether the changes I had made was tracked or not:
$ git status
and then staged it to the repository and checked whether the changes I had made was tracked or not: 
$ git add intro.html
$ git status
Then created this README.md file.

2:50pm : Now I've created a crappy-style.css file, to make my intro.html file feel less shameful.
$ git add --all / $ git add -A
This staged both my newly added files into the repository.

3:18pm : Made my first commit into the repo. YOU WILL ALWAYS HAVE TO STAGE YOUR COMMITS FIRST!!!
$ git commit -m "here's my first commit"
Then made a small change in intro.html file and checked the status.
$ git status --short
and it showed M intro.html, M meaning modified.

so you can even commit changes without writing add command, as I am going to do now:
$ git commit -a -m "updated README.md"

to view history of all your commits:
$ git log

created lalala.txt and filled it with rubbish.
$ git add -A
$ git commit -m "updated README.md and created lalala.txt"

4:00pm : Now I stuffed in some more rubbish in lalala.txt.
$ git commit -a -m "updated README.md and stuffed some more rubbish in lalala.txt"
I then renamed lalala.txt to rubbish.txt.
$ git add --all
$ git commit -m "updated README.md and created lalala.txt"



//written in intro-image branch

4:48pm : I created a new branch named intro-image.
$ git branch intro-image
$ git checkout intro-image

Then I added some relatable chess memes in intro.html.
$ git add --all
$ git status --short
A  chess-meme1.png
A  chess-meme2.jpeg
M  crappy-style.css
M  intro.html

$ git commit -m "added some chess memes in intro.html"
$ git log

ls command gives list of all the files present in the current dir.

5:32pm : made another branch named "just-remembered-something".
$ git checkout -b just-remembered-something
$ git branch

Then I made some changes in intro.html.
$ git commit -a -m "not important to know, just too lazy to type a commit message"
$ git log

Then I merged this branch with the main branch.
Before that I need to switch to the main branch.
$ git checkout main
$ git merge just-remembered-something

Since both branches were now pointing to the same commit, I deleted the just-remembered-something branch.
$ git branch -d just-remembered-something

Now, back to intro-image branch, just made some more changes to the intro.html, style.css and README.md files.
$ git add -A
$ git commit -m "added another chess meme in intro.html"
$ git status

As all the changes I had made in intro-image branch seemed fine, I decided to merge this branch with the main branch.
$ git checkout main
$ git merge intro-image
This command resulted in a conflict between the 2 branches in intro.html, which, ofcourse, I created on purpose for the sake of learning.
Then I made necessary chanegs in the file of our concern and resolved the conflict.
$ git add intro.html
$ git commit -m "resolved conflicts"
$ git branch -d intro-image

Then I went to GitHub, created this repo, copied the URL and wrote the following command:
$ git remote add origin  https://github.com/hazraChandrima/learning-git.git~ 
This means that I want to add my remote repo(in my desktop) with the URL as an origin to my local repo on GitHub.
Now, to check whether this remote origin exists, I write:
$ git remote -v
origin  https://github.com/hazraChandrima/learning-git.git~ (fetch)
origin  https://github.com/hazraChandrima/learning-git.git~ (push)

But then I realised that I didn't copy the URL correcctly. So, I removed remote origin.
$ git remote remove origin
$ git remote -v 
showed nothing, confirming that the remote origin got deleted.

$ git remote add origin  https://github.com/hazraChandrima/learning-git.git
$ git remote -v
origin  https://github.com/hazraChandrima/learning-git.git (fetch)
origin  https://github.com/hazraChandrima/learning-git.git (push)

$ git branch -M main
$ git push -u origin main

And I was done.






.
...
.....

Not yet, actually. I edited this README.md file on GitHub, and wanted to update my local Git repo as well.
$ git status
showed me:
On branch main
Your branch is behind 'origin/main' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)

nothing to commit, working tree clean.

$ git fetch origin
$ git log origin/main
$ git diff origin/main
$ git merge origin/main

$ git status
Now, it showed:
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean.
👍

This can be done in another, much shorter way as well, by using the pull command, which is a combination of fetch and pull command.
$ git diff origin/main
$ git pull origin

That's it for this repo. 😉
ok



thank you.
this line has been written in branch 2.
another line has been added.
this line has been written in branch 3.
this line has been written in branch 4.
this line has been written in branch 5.
this line has been added in branch 6.
this line has been added in branch 7.

