#Command Line for Using git
## config
### config your email and address
git config --global user.name "username in github"
git config --global user.email "email register with github"

### config editor
git config --global core.editor vim
git config --global merge.tool vimdiff

## Before using git
### generate RSA key
rsa is keeped at ~/.ssh/*
generate rsa key
```
ssh-keygen -t rsa -b 4096 -C "your@email.com"
```
### copy rsa key
cat ~/.id_rsa.pub |xclip -i
### paste key to github
### test if ssh agent is on
`eval "$(ssh-agent -s)"
### add SSH key to SSH-agent
ssh-add ~/.ssh/id_rsa
### test connect ssh
ssh -T git@github.com

## Using git
### clone repositoy
git clone git@github.com:username/reponame.git

### add file to repositoy
git add xxx
git commit -m 'comment'
------
or
git commit -a -m 'comment'

### git status
git status

### git diff
git diff
git diff --cached

### delete file
rm README
git rm README
git commit -m 'commennt'

### push
git push [remote] [branch]


