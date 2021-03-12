# github-demo
Simple demo repo to review hot to use github and git

## git configs commands:
* git config --global user.name "< user_name  >"
* git config --global user.email "< user_email >"
* git config --global --list
* git config --global core.editor "< editor >"

## initializing repo commands:
* git clone < url >
* git init

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
* git help < command >
