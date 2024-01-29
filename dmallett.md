**Forking** creates your own copy of a repository in a **remote** location (Github, Bitbucket), not on your local machine. Which is independent of the original repository. 
This means you can push changes to your own remote copy of the repository without affecting the original.

**Cloning** creates your own **local** copy of a repository on your machine. 
It's essentially a complete mirror/backup of the original and it contains all the files, commit histories, and branches of the original, remote repo.
The main difference between a github fork and git clone is that a fork creates a remote copy of the repository, stored on Github and cloning creates a copy on your local machine.

**Branching** allows you to make a *copy* of the master branch and work/modify files in parallel without affecting the main line of development. 
It also allows you to have a *pointer* to the original version/commit of the master branch so you can track differences between the two branches. 
Branching also allows you to *merge* different branches to combine different code changes and the master branch is not affected until they are merged.
