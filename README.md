#Step to add SSH key to git-hub
## list if existing .ssh key
ls -al ~/.ssh
   if existing there will be file as
>  id_rsa.pub
>  id_rsa

## Generate new SSH Key
ssh-keygen -t rsa -b 4096 -C "email@mail.com"

## Add key to SSH agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa

## copy rsa key to github account
cat ~/.ssh/id_rsa | xclip -i

