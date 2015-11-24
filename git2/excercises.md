# Exercises
The folowing exercises will contain example code in bash. Available trough __git bash__ on windows if you [installed git](https://git-scm.com/downloads). 
Though perform the "git ..." commands in e terminal as writen to learn whats intended about git.

## HELP
### I am in vim
    edit: i
    save and quit: <esc>, :wq<enter>
	quit: <esc>, :q<enter>
	quit drop changes: <esc>, :q!<enter>

## Exercises 1
Read trough the exercise first. There is an option at the end.

### Setup

Create a new folder and move in to it in you terminal.
```bash
mkdir git2days
cd git2days
```
Initiate the a new git repository in the folder
```bash
git init
```

Check what branches are in your new repository
```bash
git branch
```

Check current status
```bash
git diff
git status
git log
```
### Working directory
 
Create a file
```bash
touch file.txt
```
Check current status and log
```bash
git diff
git status
git log
```

### Stageing

Stage the file
```bash
git add file.txt
```

Check current status
```bash
git diff
git status
git log
```

### Commit 
comit the file
```bash
git commit -m "file created"
```

Check current status
```bash
git diff
git status
git log
```


### Deep stuff - meta git
This is an extra exercises if you have extra time.
It might be a litle to hard... try not to be bother with it.
__If the standard exercise seams to easy start here.__

Do the exercises 1. With the following modification
#### Setup
after part exercises 1 - setup.
move in to the .git folder
```bash
cd .git
```
init a git repo inside
```bash
git init
```
add everythng in the .git folder to git.
```bash
git add .
git commit -m "new repository"

```
move out of the .git folder

```bash
cd ..
```
#### check .git
after each part(setup/working directory...)
```bash
cd .git
git diff
git status
git add .
git commit -m "..."
cd ..
```
what has changed in the .git folder?

------

## Exercise 2
  
Read trough the exercise first. There is an option at the end.

### Lightweight Tag

now tag you commit.
```bash
git tag v0.1
```
view you tags
```bash
git tag
```

### Anotated tag
make a new commit 

```bash
touch file2.txt
git add file2.txt
git commit -m "another commit!"
```

make a annotated tag on your new commit
```bash
git tag v0.2 -m "another tag!" 
```

### deep stuff
This is an extra exercises if you have extra time.
It might be a litle to hard... try not to be bother with it.
__If the standard exercise seams to easy start here.__

#### meta git
If you did not do meta git in exercise 1 you have to start with the setup step from that.

then do excersise 2 doing "check .git" after each part. 

#### Signed tag
This is an extra extra exercises if you have extra time.
It might be a litle to hard... try not to be bother with it.

if the gpg commands fail.. install gpg
https://www.gnupg.org/download/

check if you have key
```bash
gpg --list-keys
```

if you didn't have a key you would like to use create a new one.

```bash
gpg --gen-key
```

configure git to use you key
```bash
git config --global user.signingkey 0A46826A
```

now create a signed tag..
```bash
git tag -s v1.5 -m 'my signed 1.5 tag'
```

You can also sign a commit, file or folder. 
Read more:
https://git-scm.com/book/uz/v2/Git-Tools-Signing-Your-Work

----
## Exercise 3

Form a group with 3-5 persons.

Discus and make a list of what workflows and what branches that are 

* needed in your team(s)
* bad for your team(s)

How does that compare to how you work today?

----

## Exercise 4
Read trough the exercise first. There is an option at the end.

### create branch
Create a new branch from you exsisting one

```bash
git branch ex4
```

### work on master

Create a new commit on master (with a faster syntax)
```bash
touch ex4master.txt
git commit -m "another commit!" ex4master.txt
```

look at you log
```bash
git log --oneline -graph
```

### work on your branch
Move to your new branch
```bash
git checkout ex4
```

Create a new commit
```bash
touch ex4.txt
git commit -m "another commit!" ex4.txt
```

look at you log
```bash
git log --oneline -graph
```

### view the difference between your branches

```bash
git log --oneline -graph ^master ex4
git log --oneline -graph ^ex4 master
```

### rebase your branch
```bash
git rebase master
```

### rebase master
```bash
git rebase ex4 master
```

### deep stuf - meta git
This is an extra exercises if you have extra time.
It might be a litle to hard... try not to be bother with it.
__If the standard exercise seams to easy start here.__

If you did not do meta git in exercise 1 you have to start with the setup step from that.

then do excersise 4 doing "check .git" after each part.

----
## Exercise 5
 
### create branch with new content
Start working on a new branch 
 ```bash
 git branch ex5
 git checkout ex5
 ```
 
 Create a new commit
 ```bash
 touch ex5.txt
 git commit -m "another commit!" ex5.txt
 ```
### merge your branch
```bash
git checkout master
```
try to merge with --ff-only
```bash
git merge ex5 --ff-only
```
what happens?

merge
```bash
git merge ex5 --ff-only
```
look at you log
```bash
git log --oneline -graph
```

## Excercise 6

Sign up(or sign in) for github
https://github.com/join

[Fork](https://help.github.com/articles/fork-a-repo/)
https://github.com/paven/git2-exercise



then [clone](https://help.github.com/articles/cloning-a-repository/) your fork
```bash
git clone https://github.com/<you>/git2-exercise
```
make sure you are at the master branch
```bash
git branch -v
```
###merge
```bash
git merge origin/mergeMe
git log --oneline --graph
```

push

```bash
git push
```

###now with rebase

```bash
git checkout rebaseMe
git rebase master
git checkout master
git merge --ff-only
```

push

```bash
git push
```

### no local branches

Working with detached head will speed stuff up and leave less trails
```bash
git checkout origin/rebaseMe
git rebase origin/master
git push origin HEAD:master
```

Do a commit and then redo the rebase and the push
This work flow lets you work more directly with the remote


### Deepstuff - multiple remotes

ask a colleage to work with
 
one of you gives acces to their repo to the other one.
https://help.github.com/articles/adding-collaborators-to-a-personal-repository/

```bash
git add coleage git clone https://github.com/<colleage>/git2-exercise
```
1. write a commit and post it to their repo.
2. rebase your collages rebaseMeCollege on to your master
3. what happens if you rebase and you both made changes?

## Excercise 7

### look
Open your personal
~/.gitconfig

what does it contain?
compare with another participant

open the repos local config
.git/config
```bash
git config -e
```
what does it contain?

### change

In the repos config (so that we don't change global preference)
.git/config

change editor
```bash
git config core.editor geany
```




