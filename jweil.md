*** Disclaimer: Most of my knowledge on the following three git commands came from Michael Durrant's stackoverflow post on the topic.
                I read the bulk of Michael's post twice to try to develop an understanding, and now I write based on my memory of the post.
                see: https://stackoverflow.com/questions/3329943/what-are-the-differences-between-git-branch-fork-fetch-merge-rebase-and-clon?answertab=scoredesc#tab-top

branch:
A git branch creates a 'thread' of a repository that can be developed separately (but in parallel, possibly) with the master branch.
Typically the idea is that a branch separate from the master branch will eventually be merged back into the master branch, once it is
sufficiently tested and deemed 'production' worthy. Michael Durrant explains that there are two schools of thoughts on branching:
i) use branches seldom; only branch off the master when alternative functionality is desired --- just continue updating master unless you have a good reason not to.
ii) use branches often; branch for all updates, bug fixes, etc., and only when the code in this branch is deemed production ready (or near it, at least) should
    the branch be merged with the master.
It seems that most developers probably operate somewhere on the spectrum between these two extremes.

fork:
A git fork is executed on a remote repository on which a user does not have direct modification privileges. The idea I'm getting about forks is that they are
a way to encourage nonintrusive collaboration. If a user's SSH key is registered with a certain remote repository (i.e. they have privilege to change that
repository) they will typically use git pull, make their edits, use git add and git commit, and then do a git push, which updates the original remote
repository of interest. When a user forks a repository, they create a copy of it on their own GitHub account, where they can modify the repository as they please,
and then if they wish for the original remote repository owners to integrate the forked work into the original, a pull request can be submitted.
Michael Durrant said something about pull requests that resonated with me (I paraphrase his words):
  'Pull requests' are really more like 'push requests' --- a user without privilege is 'pushing' his work to be reviewed by a user with privilege, hoping that the
  work will be integrated (merged) into the original repo. The 'pulling' is done by the 'gatekeeper' / privileged user --- the person submitting the 
  pull request is more like a pusher.


clone:
A git clone makes a full copy of a repository --- based on the reading of that single stackoverflow response, as thorough as it seemed, I am still a tad shaky
on the specifics. It sounds like the copy of the repo is local to the user's machine. It was emphasized in the response I read that the clone copies ALL of the
components of the repository --- the code, the branches, the commits and their messages, etc. I assume the use case for a copy rather than a fork (for unprivileged
users) or a pull request (for privileged users) is when somebody wishes to make extensive changes to the repo. In any case, a clone makes a full copy of a repo.
