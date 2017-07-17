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


2. to discart the modification in stage: `git reset HEAD file` then `gitcheckout —filename`


3. discart the modification after commit: `git reset --hard commit_id`

##### 6. Delete the file

1.  `git rm filename`: after commit this git, the file in both working dictionary and repository will be removed


##### 7.Add remote repository

1. `git remmote add origin git@server-name:path/repo-name.git`

   `git remote add origin https://github.com/cicifang/learnGit.git`

   : to be associated with a remote repository

2. `git push -u origin master`: to push master at the first time

3. `git push origin master`:  to push the latest

##### 8.Clone remote respository

1. `git clone git@github.com:server-name/repo-name.git`

   `git clone https://github.com/server-name/repo-name.git`

##### 9.Manage branch

1. `git branch`: to check all branches
2. `git branch <name>`: to create branch
3. `git checkout <name>`: to switch branch
4. `git checkout -b <name>`: to create and switch branch
5. `git merge <branch1>`: to merge branch1 to current branch
6.  `git merge --no-ff -m 'blabla...' <branch-name>`: a better merge commond. `--no-ff` means to disable `Fast forward` 
7. `git branch -d <name>`: to delete branch
8. `git log --graph`: to check branch-merge graph
9. `git log --graph --pretty=oneline -abbrev-commit`

##### 10.Manage tag

1. `git tag <tag-name> [commit-id]`:  to create the tag, default `HEAD`, if you don't give the commit-id
2. `git tag -a <tagname> -m "blablabla..." [commit-id]` 
3. `git show <tag-name>`: to show the statement of tag
4. `git tag`: to check all tags
5. `git push origin <tag-name>`: to push a local tag
6. `git push origin --tags`: to push all local tags
7. `git tag -d <tag-name>`: to delete a local tag
8. `git push origin :refs/tags/<tag-name>`: to delete a remote tag

##### 11.Configure alias

1. `git config --global alias.st status`
2. `git config --global alias.co checkout`
3. `git config --global alias.ci commit`
4. `git config --global alias.br branch`
5. `git config --global alias.unstage 'reset HEAD'`
6. `git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"`



