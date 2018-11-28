# Git R' Done
note:
- poll audience
- goal: learn and apply at least one new thing

SLIDE
# Basics

VSLIDE <!-- .element: style="background: white" -->
<div class="comparison">
  <img src="img/Git-Logo-1788C.png" class="fragment" data-fragment-index="1" >
  <span class="fragment" data-fragment-index="3" >!==</span>
  <img src="img/Octocat.jpg" class="fragment" data-fragment-index="2" >
</div>


note:
- Clarify the difference.  GH adds a ton of features on top of Git

VSLIDE
# Git Characteristics
<p class=stretch><img src="https://www.git-tower.com/learn/content/01-git/01-ebook/en/01-command-line/07-appendix/03-from-subversion-to-git/centralized-vs-distributed.png"></p>
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
# First things first (Branching)
1. <!-- .element: class="fragment" --> `git checkout -b cposc-contrib` <!-- .element: class="git-command" -->
 - `-b` creates the branch named `cposc-contrib`
 - `checkout` switches to the new branch
note:
-

VSLIDE
# Working locally (commit, rebase)
  - undoing changes
note:
-

VSLIDE
# Integrate your work (pull, merge vs. rebase)
note:
-

VSLIDE
# Publish/Review your work (push, pull request)
note:
-


SLIDE
# Every Day Git
1. Finding a bug in a sea of changes (blame, bisect)
1. `git log`
note:
-

VSLIDE
## When you mess up
1. Forgot file in commit?
1. Staged or committed something you shouldn't have?


SLIDE
# Resources
1. [Git - the simple guide](http://rogerdudler.github.io/git-guide/)
1. [Git Cheatsheet](http://ndpsoftware.com/git-cheatsheet.html)
1. [Oh Shit Git](https://ohshitgit.com/)
1. [Git Book (Official Docs)](https://book.git-scm.com/)
1. [Pro Git (the book)](https://git-scm.com/book/en/v2)


SLIDE
# Git Distributed/Remote Architecture
note:
- Define some terms (use a picture) http://ndpsoftware.com/git-cheatsheet.html (Pro Git Book)
  1. remote/upstream/origin
    - origin => `git remote -v` (it's an alias)


- Git can be daunting to newcomers. If you’ve not yet used Git, or just want to learn some new tricks, then bring your laptop with Git pre-installed and follow along as we cover everything you need to know to contribute to open source projects or get that next job.

To contribute to or extend open source projects, or any modern development team, you need to have a working knowledge of how to fork/merge/push to git repos. This talk will be in a tutorial format, with a live demonstration using a simple Git repo setup specifically for this talk. The audience will have the opportunity to fork the repo and follow along, including submitting their own pull request via GitHub. It will cover a wide spread of commands and their uses, including: fork, clone, branch, commit, rebase, pull, merge, push, blame, bisect, and more!


Thoughts during flight:
1. Intro: poll audience, goal: learn and apply at least one new thing
1. Clone - get a project setup
1. Git anatomy - branches; head/index/working dir
1. Tools: learn the CLI but use tools where it makes sense (merging, staging, conflict resolution)
1. Working individually: Add, commit, push, pull
1. Working with a team: branch, pull request, rebase (squash), rebase (sync) vs merge
1. Debugging: bisect, blame, grep (log -S)
1. Contributing to open source: fork, upstreams
1. Automate: Git hooks, aliases, .gitconfig (e.g. [pager] after latest update)
1. Questions


# General Flow
1. Setup (clone) a project and start making changes on the main branch (Single User)
2. Thats great, but almost no one works like this,  Git branches are cheap/easy so use them. (Team Development)
  - Branch per feature/fix
  - Managing conflicts/change (rebase vs. merge)
3. This is CPOSC, What about open source?
  - Fork -> origin + upstream and keeping them in sync, submitting pull request
  - A note about open source contributing: be nice, style guides, no feature
4. You said I'd learn some new tricks?
  - aliases
  - commit hooks
  - git bisect
  - git blame
