

# Prerequisites
A participant is expected to know how to use the following git commands
* add
* rm
* push
* pull
* commit
* log
learn them at https://git-scm.com/ or https://www.codecademy.com/courses/learn-git

Participants need:
Git installed on a computer(preferably linux) with access to internet.Git installed on a local computer.

I need:
Access to internet
Projector (preferably HDMI or VGA)

---

    [![CC-BY-SA 4.0](../res/ccbysaPurple.png)](http://creativecommons.org/licenses/by-sa/4.0/) Patrik Gustafsson, Purple Scout AB


---

Internaly usage of git

branch
commit

---

# Why are you here?
To raise your awareness of
 * git does and don'ts
 * git workflows
 * some in depth git mechanics.

---

# Why am I here?

    I believe that the best way to evolve is to teach.

I thrill on
* (FL)openscource(s)
* tools
* teaching
* problem solving
* code

---

# Who am I?

Titles:
* Senior Software Shaman
* Toolmaster
* Public speaker

https://www.linkedin.com/in/paven
http://www.purplescout.se/project/patrik-gustafsson/
https://github.com/paven/birGit

---

# Short Introduction Git
* Distributed
* Fast
* Commit centered
* SHA everything
* Filesystem storage
<!--_Introduction to Git (Nice to have)_-->

---

# Git basics
master:

```bash
git init
git branch -v
```

origin:

```bash
git clone https://github.com/paven/birGit.git
git remote -v
git branch -av
```

---

# Git basics - Stageing

```bash
echo "filechange" >> file
git add file
git commit -m "commit message"
```
<!--_The Index (Mandatory)_-->

---

# Git basics - directory magix

your folder is your working direktory
your folder is as is no magix

.git is your repository history ands then some

<!-- _Working Directory (Mandatory)_
_Recording Changes to the Repository (Mandatory)_
-->

---

# Git basic - history

```bash
git log
git log --oneline --graph
```

---

# Git basic - the commit

```bash
git cat-file commit HEAD
```

--

```bash
(printf "commit %s\0" $(git cat-file commit HEAD |
wc -c);
git cat-file commit HEAD) |
sha1sum
```



<!--_Authors and Committers (Mandatory)_-->

---

# Index, stageing


---

# Under the hood - replace by usage.
* .git
_Git Repository (Mandatory)_
_The Git Directory (Nice to have)_
_The Treeish (Nice to have)_
_Git Objects (Nice to have)_
The commit-ish

---

# Workflows 
* Rebase Workflow
* Branching strategies
* Gerrit Workflow
* Git flow or not.
_Release branch (Mandatory)_
_Branching Workflows (Mandatory)_
_Branch Management (Mandatory)_
_Keeping Central repository clean (Mandatory)_
_Aggregating commits (Mandatory)_

_Switching between releases (Mandatory)_ ?
_Managing maintenance release (Mandatory)_ ?

---

# Tags - Release
_Tagging (Mandatory)_
_Using Tags for releases (Mandatory)_
_Major releases (Mandatory)_
_Using Tag description for major release summarizing changes (Nice to have)_


(maybe)_Using Repository History to create Change Log (Nice to have)_

---

# Working with Branches and remotes
* Branch:
_Branch Management (Mandatory)_

* Rebase:
_Rebasing (Mandatory)_
_Rewriting History (Mandatory)_
_Interactive Staging (Mandatory)_
_Aggregating smaller changes into bigger one (closer to the business) (Mandatory)_
_Grouping commits into logical parts (Mandatory)_
_Keeping Central repository clean (Mandatory)_

* Remotes:
Github
_Distributed repositories (Mandatory)_
_Working with Remotes (Mandatory)_
_Hosted Git ~~(CollabNet TeamForge) (Mandatory)~~_

* Merge:
_Branching and Merging (Mandatory)_
_Remote Branches (Mandatory)_

---

# Nested repos - overview
* Hows:
_Submodules (Mandatory)_
_Subtree Merging (Mandatory)_

* Whys and why notes:
_How to divide logically application and the repository (Nice to have)_

---

# Undoing Things
_Undoing Things (Mandatory)_
_Revision Selection (Mandatory)_ 

---

# Debugging
_Debugging with Git (bisect) (Mandatory)_

---

# Config
_Ignores and Excludes (Mandatory)_
_Git Configuration (Nice to have)_
_Git Attributes (Nice to have)_
_Git Hooks (Nice to have)_

---

# Gerrit
* Code review: _Code reviews (Gerrit) (Mandatory)_
_Creating structure for aggregating and reviewing changes from developers (Mandatory)_
* Verified:
_Testing and Staging environment (Nice to have)_

---

# GUI
* your IDE (ex IDEA)
* gitk
* git gui
alternatives: like tortoisegit, SmartGitHg

_Git Commands Git via GUI (GIT Extensions or similar) (Mandatory)_

---

# Requested and processed

*

---

# Git Basics

--

# Git Concepts

---

# Git Branching

---

# Git Plumbing and Advanced topics

---

# Git on the Server

---

# Git Tools

---

# Customizing Git

---

# Automatic deployment via GIT

---

# Documentation, Release Change Log

---

# Central Repo Push and Pull Strategies

---

# Software Architecture and Components

---





# Not included in course
Hosted Git (CollabNet TeamForge) (Mandatory) Though github will be used

Non-SCM Uses of Git (Nice to have)

Merging works via e-mail (Nice to have)
Merging works from others repositories (Nice to have)
Octopus merge (Nice to have)

Signatures (Nice to have)

The Protocols (Nice to have)

Generating SSH Public Key (Nice to have)

Production repository (Nice to have)
How to manage libraries and subprojects develop by third parties (Nice to have)
Using submodules to automate upgrades (Nice to have)

---