# Learn to use Git

>This note is from [here](https://www.liaoxuefeng.com)

##### 1. Initialize a Git respository 

  `git init`

##### 2. Add files to Git respositoy 
  step1. `git add <filename>`: add files from working dictionary to stage

  step2. `git commit -m "note of this commit"`: commit files from stage to the the current branch

##### 3. Check the status of working derictory 

  ` git status`

  ` git diff`

##### 4. Check the history

  `git log`: check the commit history

  `git reflog`: check the command history

##### 5. Undo modify the file under different conditions

1. to discart the modification in working directory: `git checkout --filename`


2. to discart the modification in stage: `git reset HEAD file` then `git checkout —filename`


3. discart the modification after commit: `git reset --hard commit_id`

##### 6. Delete the file

  `git rm filename`





 


