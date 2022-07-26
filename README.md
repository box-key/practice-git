# Practice Git!

## Practice fetch
* `git fetch origin` copies all data in the remote repo. All remote branches can be referenced by `origin/<branch_name>`. E.g., `origin/master` is different from `master`
* `git fetch origin <branch_name>` copies a remote branch into local. It can be referenced by `origin/<branch_name>`
* Note that `git fetch` copies all changes on the remote repo into the local. For example, I fethced `branch_x` before someone made changes to `branch_x` on the remote repo. Then, when I do `git fetch origin branch_x`, this will override `origin/branch_x` on my local repo

## Practice rebase
* `git rebase` is a way to merge branches
* The difference between `git merge` is that `git merge` creates a commit every time you merge a branch into other. This can mess up a project history. On the other hand, `git rebase` moves local commits to the tip of the branch you want to merge into the local branch. This can result in a perfectly linear, much cleaner project history. However, this is a double-edged sword because `git rebase` re-writes a project history. 
* As a rule of thumb, you should only `git rebase` a local branch onto a public branch 

## Practice push
* `git push origin <my_local>:<my_remote>` is used to push `<my_local>` branch to `<my_remote>` branch on the remote repo

## Undo local commit

### Checkout Approach
1. `git checkout <commit_hash>`, which changes the current working directory back to the working directory associated with the commit hash
1. `git branch <branch_name>` 
1. `git merge <branch_name>` to merge the working directory that undid the changes into the current branch

This approach keeps the commits that you undid in a project history. So if you do `git log`, you will see the undid commits in the log 

### Reset Approach
1. `git reset --hard HEAD~<n>`. You can omit `n` if you want to undo the previous commit. Use `n` if you want to undo more commits, e.g., HEAD~3 refers to the third commits from the `HEAD`

### Revert Approach


This approach completely rewrites a project history so you don't see the undo commits in `git log`

## Notes Misc.
* `tracking_branch` is a local branch which is tied to a remote branch. If I do `git pull` on a tracking branch, it automatically fetches from the remote branch and merges it to the local branch. To set up a remote branch, use `git branch -u origin/<remote_branch>` on a local branch that you want to be a tracking branch for `origin/<remote_branch>`
* `<commit_hash>^` is used to refer to the parent of the commit. E.g., `HEAD^` refers to the parent of the `HEAD`. You can specify a number after the `^` to identify which parent you refer to, e.g., `HEAD^3` is the third parent of `HEAD`. `~` is the same..?

