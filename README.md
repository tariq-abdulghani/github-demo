# github-demo
Simple demo repo to review hot to use github and git


## git configs commands:
* git config --global user.name "< user_name  >"
* git config --global user.email "< user_email >"
* git config --global --list
* git config --global core.editor "< editor >"
* git config --global diff.tool "< visual_diff_tool >"

## initializing repo commands:
> we can create git repo locally first or from
> github repo.
* git clone < url >
* git init [ < dir_name > ]
> if dir_name is not provided git will initialize current
> dir as a git repo.

## basic commands:
* git status
* git ls-files  #to list tracked files
* git add < file-name >
* git commit -m "< comment >"
* git push < remote > < branch >
* git pull < remote > < branch >

## Undoing Things:
* git restore --staged < file >..." to unstage.
* git restore < file >..." to discard changes in working directory

* git checkout < commit_id > **is safe to use**
* git revert < commit_id >
>reverts only that commit.
* git reset < commit_id >
>restores the project to that commit all commits after are removed


>As said, using the reset command on your HEAD branch is a quite drastic action: it will remove any commits (on this branch) that came after the specified revision. If you're sure that this is what you want, everything is fine.
>However, there is also a "safer" way in case you'd prefer leaving your current HEAD branch untouched. Since "branches" are so cheap and easy in Git, we can easily create a new branch which starts at that old revision:

* git checkout -b old-project-state 0ad5a7a6

## Moving / Deleting files:
* git mv < old_name > < new_name >
* git rm < file_name > #removes file that is tracked
  for deleted files if we want to revert deleting
  we need to do it in two steps
  first restore --staged
  second restore

  because unstaging  means just don't put changes in staging state
  but restoring the file is just discard the last changes.


## Utils:
* git log
>git log --graph --oneline --decorate --all
* git show < commit_it >
* git help < command >

## Comparisons:
  >note if you've configured difftool you cna replace
  >each diff with difftool in the following statements.

* git diff #compares working dir to the staging area
* git diff HEAD #compares working dir against last commit
* git diff --cached HEAD #compares staging area to the last commit


## Branching & Merging.
* git branch -a 
>list all branches local or remote.
* git branch "< branch_name >"
> creates new branch
* git checkout < branch_name >
>switch to given branch name and updates files with HEAD 
* git branch -m < old-branch-name > < new-branch-name>
> to rename a branch
* git branch -d < branch-name >
> to delete a branch
* git merge < branch_that_you_merge_to_your_current_branch >
> if u want to merge to master u need to be in master first then 
> merge the other branch to master

* git merge --no-ff < branch_that_you_merge_to_your_current_branch >
> no fast forward merge it will keep branching topology

>**Automatic Merges:**
when u work on a branch and other commit to the brach you
want to merge with but they change files other than yours.
>**Conflicting Merges:**
when u do commits to single file from different branches .


## Stashing (saving changes in temp dir and checkout to the last commit)
* git stash
* git stash list
* git stash apply  < stash_name >
* git stash pop
>retrieves the latest stash from stash stack
