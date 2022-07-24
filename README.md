# Practice Git!

## Practice fetch!
* `git fetch origin` copies all data in the remote repo. All remote branches can be referenced by `origin/<branch_name>`. E.g., `origin/master` is different from `master`
* `git fetch origin <branch_name>` copies a remote branch into local. It can be referenced by `origin/<branch_name>`
* Note that `git fetch` copies all changes on the remote repo into the local. For example, I fethced `origin/branch_x` before and someone made changes to `origin/branch_x` on the remote repo. Then, when I do `git fetch origin branch_x`, this will override `origin/branch_x` on my local repo

## Practice push!
* `git push origin <my_local>:<my_remote>` is used to push `<my_local>` branch to `<my_remote>` branch on the remote repo
* Hello
* Hello again
