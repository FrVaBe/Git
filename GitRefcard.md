# FrVaBe Git Refcard

## Branching

**list**  
`$ git branch`  
<small>list all local branches</small>  
`$ git branch -av`  
<small>list all local and remote branches</small>

**create**  
`$ git branch <name_of_new_branch>`  
<small> create a new branch</small>  
`$ git checkout -b <name_of_new_branch>`  
<small> create a new branch and switch to it</small>

**merge**  
`$ git merge <name_of_branch>`  
<small>merge branch (_name_of_branch_) on top of the current branch</small>

**delete Branch**  
`$ git branch -d <name_of_branch>`  
<small>delete local branch</small>  
`$ git push origin --delete <name_of_branch>`    
<small>delete remote branch</small>  
`$ git fetch --prune`  
<small>fetch branches (update remote-tracking branches) and remove any remote-tracking references that no longer exist on the remote</small>

**rebase**  
`$ git checkout <name_of_branch>`  
`$ git rebase master`  
<small> moves the branch (_name_of_branch_) on the tip of the master branch</small>

## Stashing

**create**  
`$ git stash [<message>]`  
<small>put uncommited changes to the stash area and revert project to match HEAD</small>  
`$ git stash --include-untracked [<message>]` or  
`$ git stash save -u [<message>]`  
<small>put uncommited changes **and untracked files** to the stash area and revert project to match HEAD; alternative `add` untracked files before stash</small>

**list and show**  
`$git stash list`  
<small>list stashed modifications</small>  
`$git stash show <name_of_stash>`  
<small>inspect stashed modification, e.g. *git stash show stash@{1}*</small>

**restore**  
`$git stash pop [<name_of_stash>]`  
<small>remove a single stashed state from the stash list and apply it on top of the current working tree state; _stash@{0}_ is assumed when no _<name_of_stash>_ is given</small>  
`$git stash apply [<name_of_stash>]`  
<small>like pop, but do not remove the state from the stash list; _stash@{0}_ is assumed when no _<name_of_stash>_ is given</small>  
`$git stash drop [<name_of_stash>]`  
<small>remove a single stash entry from the list of stash entries;  _stash@{0}_ is assumed when no _<name_of_stash>_ is given</small>


