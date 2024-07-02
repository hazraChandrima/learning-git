//written in main branch

This repository is just made to teach myself Git.
2-7-24,2:31pm : Just learnt:
git --version
git config --global usesr.name "chandrima-hazra"
git config --global user.email "hazrachandrima6@gmail.com"
mkdir july-proj 
cd july-proj (C:Users\user\july-proj)
then initialised an empty git repo in folder july-proj:
git init 
then created a naked intro.html file and checked whether the changes I had made was tracked or not:
git status
and then staged it to the repository and checked whether the changes I had made was tracked or not: 
git add intro.html
git status
then created this README.md file.

2:50pm : Now I've created a crappy-style.css file, to make my intro.html file feel less shameful.
git add --all / git add -A
This staged both my newly added files into the repository.

3:18pm : Made my first commit into the repo. YOU WILL ALWAYS HAVE TO STAGE YOUR COMMITS FIRST!!!
git commit -m "here's my first commit"
Then made a small change in intro.html file and checked the status 
git status --short
and it showed M intro.html, M meaning modified.

so you can even commit changes without staging, as I am going to do now:
git commit -a -m "updated README.md"

to view history of all your commits:
git log

created lalala.txt and filled it with rubbish.
git add -A
git commit -m "updated README.md and created lalala.txt"

4:00pm : Now I stuffed in some more rubbish in lalala.txt
 git commit -a -m "updated README.md and stuffed some more rubbish in lalala.txt"
I then renamed lalala.txt to rubbish.txt
git add --all
git commit -m "updated README.md and created lalala.txt"



//written in intro-image branch

4:48pm : I created a new branch named intro-image.
git branch intro-image
git checkout intro-image

Then I added some relatable chess memes in intro.html.
git add --all
git status --short
A  chess-meme1.png
A  chess-meme2.jpeg
M  crappy-style.css
M  intro.html

git commit -m "added some chess memes in intro.html"
git log

ls command gives list of all the fiels present in the current dir.


