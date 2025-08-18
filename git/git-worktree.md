# Git Worktree

Just was reminded today about git worktree, and thought maybe I should dig more into it and add to this repo. I want to try to start using it more in my projects. The following scenario frequently comes up for me:

- Working hard on a feature and everything is taken apart while I'm in the weeds
- Coworker asks for a bug fix or GH PR review
- I stash my changes using `git stash`
- I checkout the other branch, do whatever I need to do, sometimes committing or even making a new stash entry
- I have to recheckout my other branch, unstash, things can get messy easily if you don't do things in the right order.

Enter git worktree.

Now the workflow would instead look like this:

- From main repository (although there are several ways to set up your main repo folder)
  - `git worktree add ../my-cool-feature
  - `cd ../my-cool-feature` (this worktree now lives alongside the original repo if you are following this path)
- Working hard on a feature and everything is take apart while I'm in the weeds.
- Coworker asks for a bug fix or GH PR review
- `cd ../main-repo`
- `git worktree add ../bug-fix`
- `cd ../bug-fix`
- Fix the bug, commit, push, so on
- `cd ../my-cool-feature`
- `git worktree remove bug-fix`

If I understand it right, I think that should be all there is - your original feature and other worktrees will stay perfectly intact. I'll be diving into this in the next week and either update this or add more as I come to understand the best workflows better.

https://git-scm.com/docs/git-worktree
