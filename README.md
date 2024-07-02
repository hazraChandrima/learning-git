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
