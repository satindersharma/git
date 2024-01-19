# git
git realated


--global is ment ot write to global i.e ~/.gitconfig rather than the repository .git/config
one day = 86400 seconds
 two day = 172800 seconds

`git config --global credential.helper 'cache --timeout=172800'`

`git pull origin master`

`git config --list`

`git config --global user.name` 

`git config --global user.email`


reset
If you don't care about your local changes, try to reset it to HEAD (original state), e.g.

`git reset HEAD --hard`


### to only allow pull or restric ton push


git config branch.master.pushRemote no_push


##### file in gitignore but still exists in commit
###### this is because we have commited the file once 
###### (once it commited it will be there no matter how many time you put it in gitignore)

## delete the file from locally and also from the github
`git rm -r --cached <folder_name/file_name>`


## Add git with token
### go to your github
##### go to `settings` > `develper settings` > `Personal access tokens` > `fine grained tokens`
##### go to `settings` > `develper settings` > `Personal access tokens` > `classic tokens` # check the repo section for permission



export GITHUB_USER=magickatt

export GITHUB_TOKEN=secret

export GITHUB_REPOSITORY=magickatt/ContainerisingLegacyApplicationsTalk

git clone https://${GITHUB_USER}:${GITHUB_TOKEN}@github.com/${GITHUB_REPOSITORY}




### make `satinder` branch same as `dev` branch

#### `git checkout satinder`
#### `git reset --hard dev`
#### `git push --force origin satinder`



#### `git clone https://username:token@github.com/username/repo1`




#### revert the commit statement(and keep the file changes
when you done git add . and git commit -m "change" but want to cancel this commit and keep the file changes
#### `git reset --soft HEAD~`

similary
1 - Undo commit and keep all files staged: `git reset --soft HEAD~`

2 - Undo commit and unstage all files: `git reset HEAD~`

3 - Undo the commit and completely remove all changes: `git reset --hard HEAD~`



### remove a file from tracing locally, but kept the file on github
git update-index --skip-worktree <file>
git rm --cached django.log --sparse
