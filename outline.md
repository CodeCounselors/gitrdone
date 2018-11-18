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

SLIDE
# Git != GitHub/GitLab/etc
note:
- Clarify the difference.  GH adds a ton of features on top of Git

SLIDE
# Your first project (Clone)
note:
-

SLIDE
# Your workspace
  1. workspace/index

SLIDE
# Working locally (commit, rebase)
  - undoing changes
note:
-

SLIDE
# Making a contribution (branching)
note:
-

SLIDE
# Integrate your work (pull, merge vs. rebase)
note:
-

SLIDE
# Publish/Review your work (push, pull request)
note:
-

# Git Distrubuted/Remote Architecture
note:
- Define some terms (use a picture) http://ndpsoftware.com/git-cheatsheet.html (Pro Git Book)
  1. remote/upstream/origin
    - origin => `git remote -v` (it's an alias)

SLIDE
# Finding a bug in a sea of changes (blame, bisect)
note:
-


- Git can be daunting to newcomers. If you’ve not yet used Git, or just want to learn some new tricks, then bring your laptop with Git pre-installed and follow along as we cover everything you need to know to contribute to open source projects or get that next job.

To contribute to or extend open source projects, or any modern development team, you need to have a working knowledge of how to fork/merge/push to git repos. This talk will be in a tutorial format, with a live demonstration using a simple Git repo setup specifically for this talk. The audience will have the opportunity to fork the repo and follow along, including submitting their own pull request via GitHub. It will cover a wide spread of commands and their uses, including: fork, clone, branch, commit, rebase, pull, merge, push, blame, bisect, and more!
