# Git R' Done
### This talk
https://codecounselors.github.io/gitrdone
### Git Repository
https://github.com/CodeCounselors/gitrdone
#### Brought to you by
<a href="http://www.codecounselor.org">Nate Good</a> / <a href="http://twitter.com/codecounselor">@codecounselor</a></small>
note:
- poll audience
- goal: learn and apply at least one new thing


SLIDE
# First Things First
<div class="comparison fragment" data-fragment-index="1">
  <img src="img/Git-Logo-1788C.png" class="fragment" data-fragment-index="3" >
  <span class="fragment" data-fragment-index="5" >!==</span>
  <img src="img/Octocat.jpg" class="fragment" data-fragment-index="4" >
</div>
note:
- Clarify the difference.  GH adds a ton of features on top of Git

VSLIDE
# Git Characteristics
<p class=stretch><img src="img/gitsvn.png"></p>
note:
- distributed, remote
- Not a talk about comparing SCM systems but git was a bit of a game changer

VSLIDE
# Tools?
- Terminal ([Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh/wiki/Cheatsheet#git), [Oh My Bash](https://github.com/ohmybash/oh-my-bash))
- Git Clients (SourceTree, Tower, IDEs, etc)
- OS Integrations (TortoiseGit)
- Diff Tools (IDEs, KDiff, etc)
note:
- right how, a terminal.  
- introduce new ones as we go; discuss briefly
- learn the CLI but use tools where it makes sense (merging, staging, conflict resolution)




SLIDE
# Let's Git Started

VSLIDE
# Install Git
- https://git-scm.com/download or package manager of your choice
- Basic Setup https://help.github.com/articles/set-up-git/
  - `git config --global user.name "John Doe"` <!-- .element: class="git-command" -->
  - `git config --global user.email "email@example.com"` <!-- .element: class="git-command" -->
  - `git config --global --list` <!-- .element: class="git-command" -->
- Github Authentication (HTTPS or SSH)
  - https://help.github.com/articles/set-up-git/#next-steps-authenticating-with-github-from-git
note:

VSLIDE
# git clone
<!-- .element: fragment="file" -->
1. cd `~/projects` <!-- .element: class="file" -->
1. [git clone git@github.com:CodeCounselors/gitrdone.git](https://github.com/CodeCounselors/gitrdone) <!-- .element: class="git-command" -->
1. cd `gitrdone` <!-- .element: class="file" -->
note:
-

VSLIDE
# Now we modify things
1. Make a local change to `contrib/cposc.md` <!-- .element: class="file" -->
1. <!-- .element: class="fragment" --> `git status` <!-- .element: class="git-command" -->
1. <!-- .element: class="fragment" --> touch `new.txt` <!-- .element: class="file" -->
1. <!-- .element: class="fragment" --> `git status` <!-- .element: class="git-command" -->
  - <!-- .element: class="fragment" --> `Changes not staged for commit` <!-- .element: class="git-text" -->
  - <!-- .element: class="fragment" --> `Untracked files` <!-- .element: class="git-text" -->
1. <!-- .element: class="fragment" --> `git add contrib` <!-- .element: class="git-command" -->
1. <!-- .element: class="fragment" --> `git status` <!-- .element: class="git-command" -->
  - <!-- .element: class="fragment" --> `Changes to be committed` <!-- .element: class="git-text" -->
1. <!-- .element: class="fragment" --> `git commit -m "my first contribution"`  <!-- .element: class="git-command" -->
  - <!-- .element: class="fragment" --> `Your branch is ahead of 'origin/<branch>' by 1 commit` <!-- .element: class="git-text" -->

VSLIDE
# What did we just do?
<p class=stretch><img  src="https://devopscube.com/wp-content/uploads/2015/08/GIT-BASICS.png"></p>

TODO: Make my own image reflecting this repo (hashes)

[Interactive Git Cheatsheet](https://ndpsoftware.com/git-cheatsheet.html)
note:
-workspace/index

VSLIDE
# One last thing
1. <!-- .element: class="fragment" --> `git push`  <!-- .element: class="git-command" -->
1. Oh no, what happened? <!-- .element: class="fragment" -->
    - <!-- .element: class="fragment" --> `ERROR: Permission to <repo> denied to <user>.` <!-- .element: class="git-text" -->




SLIDE
# Working with Others
1. Working with a team (cloned)
2. Working on open source (forked)
note:
-

VSLIDE
# Your own branch
1. <!-- .element: class="fragment" --> `git checkout -b cposc-contrib` <!-- .element: class="git-command" -->
 - `-b` creates the branch named `cposc-contrib`
 - `checkout` switches to the new branch
note:
- Mention aliases here
- Talk about -v, --v, --remote

VSLIDE
# A Tidy History (Interactive Rebase)
1. make a few commits
1. combine them into one
note:
-

VSLIDE
# Contribute to Project
1. Create pull request
note:
-

VSLIDE
# Contribute to Open Source
1. Setup upstream
1. Fork Repo
1. Setup origin to track fork
note:
-

VSLIDE
# Submit your first Pull Request
1. Push branch
1. Create pull request
note:
-




SLIDE
# Every Day Git

#### A Pro Git User is:
#### <!-- .element: class="fragment blue" -->imperfect
#### <!-- .element: class="fragment red" -->efficient
#### <!-- .element: class="fragment green" -->careful
#### <!-- .element: class="fragment orange" -->aware
#### <!-- .element: class="fragment magenta" -->lazy
note:
- imperfect: how to fix mistakes
- efficient: use aliases and tools to cut down on redundant tasks (e.g. pushing new branch)
- careful: read the documentation (e.g reset --hard, don't just copy/paste Stack Overflow)
- aware: There is a lot to Git, know what it can do for you
- lazy: hooks, .gitconfig (e.g. pager), etc.

SLIDE
# When you mess up
1. Forgot a file in commit? <!-- .element: class="fragment" -->
  - `git commit --amend` <!-- .element: class="git-command" -->
1. Committed something you shouldn't have? <!-- .element: class="fragment" -->
  - `git reset --soft HEAD~` <!-- .element: class="git-command" -->
1. Something broke but you have no idea when or where? <!-- .element: class="fragment" -->
  - `git bisect` <!-- .element: class="git-command" -->
1. Accidentally wiped out changes you now need? <!-- .element: class="fragment" -->
  - `git reflog` <!-- .element: class="git-command" -->
    - (If you committed them, otherwise use a good IDE)
note:
- if something was staged, just use a GUI to unstage files or hunks (demo SourceTree)

VSLIDE
# Amend a commit
#### WARNING: Rewrites history <!-- .element: class="warning" -->
#### `git commit --amend` <!-- .element: class="git-command" -->
1. Changing a commit message at `HEAD`<!-- .element: class="git-text" -->
2. Adding more changes to the previous commit
----
#### `git rebase --interactive` <!-- .element: class="git-command" -->
1. Amending a commit farther back in the history
2. combining, reordering, or deleting commits

VSLIDE
# Undo ... Undo!
#### `git reset --soft HEAD~` <!-- .element: class="git-command" -->
note:
- "git undo" use case: stash on the branch instead of stash

VSLIDE
# Who's Fault is it?
`git blame` <!-- .element: class="git-command" --> (annotate)

(But if that doesn't help, `bisect`<!-- .element: class="git-command" --> to the rescue!)

VSLIDE
# git-bisect
####  `binary search to find the commit that introduced a bug`

1. <!-- .element: class="fragment" -->Find a commit that works as expected (e.g. `381147c`<!-- .element: class="git-text" -->)
1. <!-- .element: class="fragment" -->`git bisect start`<!-- .element: class="git-command" -->
1. <!-- .element: class="fragment" -->`git bisect bad`<!-- .element: class="git-command" --> (assuming the `HEAD`<!-- .element: class="git-text" --> is bad)
1. <!-- .element: class="fragment" -->`git bisect good`<!-- .element: class="git-command" --> &nbsp;`381147c`<!-- .element: class="git-text" -->
1. for each revision, execute one of: <!-- .element: class="fragment" -->
  - `git bisect good`<!-- .element: class="git-command" -->
  - `git bisect bad`<!-- .element: class="git-command" -->
1. <!-- .element: class="fragment" -->`git bisect reset`<!-- .element: class="git-command" -->

<!-- .element: class="fragment" -->Tip: You can provide a command to automate the good/bad check

SLIDE
# Aliases and Functions

SLIDE
# Commit Hooks
## (To the Rescue)
### `gitrdone/.git/hooks` <!-- .element: class="file" -->

VSLIDE
# Decorative Hooks

VSLIDE
# Safety Hooks

VSLIDE
# Notification Hooks




SLIDE
# Questions?
------------
### Resources
1. [Git - the simple guide](http://rogerdudler.github.io/git-guide/)
1. [Git Cheatsheet](http://ndpsoftware.com/git-cheatsheet.html)
1. [Oh Shit Git](https://ohshitgit.com/)
1. [Git Book (Official Docs)](https://book.git-scm.com/)
1. [Pro Git (the book)](https://git-scm.com/book/en/v2)


SLIDE
# Didn't make the cut
- `grep (log -S)`
