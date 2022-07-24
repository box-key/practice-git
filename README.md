# Practice Git!

## Practice fetch!
* `git fetch origin` copies all data in the remote repo. All remote branches can be referenced by `origin/<branch_name>`. E.g., `origin/master` is different from `master`
* `git fetch origin <branch_name>` copies a remote branch into local. It can be referenced by `origin/<branch_name>`
* Hey!

## Practice rebase
* `git rebase` is a way to merge branches
* The difference between `git merge` is that `git merge` creates a commit every time you merge a branch into other. This can mess up a project history. On the other hand, `git rebase` moves local commits to the tip of the branch you want to merge into the local branch. This can result in a perfectly linear, much cleaner project history. However, this is a double-edged sword because `git rebase` re-writes a project history. 
* As a rule of thumb, you should only `git rebase` a local branch onto a public branch 
* Hey!
