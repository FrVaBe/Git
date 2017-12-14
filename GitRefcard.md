# FrVaBe Git Refcard

## branch

**list**  
`$ git branch`  
<small>list all local branches</small>

`$ git branch -av`  
<small>list all local and remote branches</small>

**create**  
`$ git branch [name_of_new_branch]`  
<small> create a new branch</small>

`$ git checkout -b [name_of_new_branch]`  
<small> create a new branch and switch to it</small>

**mergen**  
`$ git merge [name_of_branch]`  
<small>merge branch (_name_of_branch_) on top of the current branch</small>

**delete Branch**  
`$ git branch -d [name_of_branch]`  
<small>delete local branch</small>  
`$ git push origin --delete [name_of_branch]`    
<small>delete remote branch</small>

`$ git fetch --prune`  
<small>fetch branches (update remote-tracking branches) and remove any remote-tracking references that no longer exist on the remote</small>

**rebase**  
`$ git checkout [name_of_branch]`  
`$ git rebase master`  
<small> moves the branch (_name_of_branch_) on the tip of the master branch</small>
