#### Global Git Configuration
##### Set alias for git command
```
alias g='git'
```

##### Set git command alias in gitconfig file
```
curl https://raw.githubusercontent.com/sgyyz/gitconfig/master/gitconfig > ~/.gitconfig
```

##### Set git commit user information
#Global Configuration#
```
git config --global user.name "your name"
git config --global user.email "your email"
```
#Repository Configuration#
Remove the `--global` flag in above command. And you can check it via `git config --list`.

#### Tips
##### Sync Remote Branch
```
git fetch -p

### Delete not existing branches on remote
git branch -vv | grep ': gone]' | awk '{print $1}' | xargs git branch -d
or
git branch -vv | awk '/: gone]/{print $1}' | xargs git branch -d
```
