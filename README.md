# git
git realated


--global is ment ot write to global i.e ~/.gitconfig rather than the repository .git/config
one day = 86400 seconds
 two day = 172800 seconds

`git config --global credential.helper 'cache --timeout=172800'`

`git pull origin master`

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

`git rm -r --cached <folder_name/file_name>`
