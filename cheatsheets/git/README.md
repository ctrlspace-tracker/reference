
#### Git Add ssh key commands
```
ssh-keygen -t rsa -b 4096 -C "deivee@gmail.com"
eval "$(ssh-agent -s)"
ssh-add -K ~/.ssh/id_pers_rsa
pbcopy < ~/.ssh/id_rsa.pub
git clone git@github.com:ctrlspace-tracker/reference.git 
```

### Initialize a repository
```
git init

git add .
git commit -m <commit message> (Commit files to local repository)
git push
```

### Git basic commands
```
git add .
git commit -m "test command here"
git push

git status      // Shows the current status of the working directory
git diff        // Shows the difference in changes between the working directory and the repo

```

### Remote repository
```
git remote
git remote -v
```

### Git pull latest from develop 

### Logging
```
git log
git log --all
git log --all --oneline --decorate --graph
```

### Branches

#### New branch and commit
```aidl
git branch —list            //(shows all the branches). 
git checkout -b develop     // (creates a local branch called develop)change a file
git add .
git commit -m "Comments"    
git push —set-upstream origin develop
```

#### Merge with parent branch

Local repository A (Branch)
When you are pointing to the local repository
```aidl
git checkout develop
git merge A
git push
```

#### Deleting a remote branch
