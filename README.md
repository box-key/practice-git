# Practice Git!

## Practice fetch
* `git fetch origin` copies all data in the remote repo. All remote branches can be referenced by `origin/<branch_name>`. E.g., `origin/master` is different from `master`
* `git fetch origin <branch_name>` copies a remote branch into local. It can be referenced by `origin/<branch_name>`
* Note that `git fetch` copies all changes on the remote repo into the local. For example, I fethced `branch_x` before someone made changes to `branch_x` on the remote repo. Then, when I do `git fetch origin branch_x`, this will override `origin/branch_x` on my local repo

## Practice push
* `git push origin <my_local>:<my_remote>` is used to push `<my_local>` branch to `<my_remote>` branch on the remote repo

## Notes
* `tracking_branch` is a local branch which is tied to a remote branch. If I do `git pull` on a tracking branch, it automatically fetches from the remote branch and merges it to the local branch. To set up a remote branch, use `git branch -u origin/<remote_branch>` on a local branch that you want to be a tracking branch for `origin/<remote_branch>`
* `<commit_hash>^` is used to refer to the parent of the commit. E.g., `HEAD^` refers to the parent of the `HEAD`. You can specify a number after the `^` to identify which parent you refer to, e.g., `HEAD^3` is the third parent of `HEAD`. `~` is the same..?
