## Disclaimer
This is not a good guide. This is my guide that I use to push my stuff up from other PCs.

Although it's not in any perfect order, or is the "Best practices" which require lots of wherewithall...

...this still may be somewhat helpful to you. 


### 1. install Git

    sudo apt-get install git

### 2. configure Git 

    git config --global user.name "github_username"

    git config --global user.email "youremail@email.com"

### 3. If making something new
browse to chosen directory, preferably blank

    git init <REPONAME>

### Be nice and make a README
Make it in MARKDOWN format (hence the .md extension)

    nano README.md
    

### IS the SSH agent running?

    ps -e | grep [s]sh-agent 

### If not, start it

    ssh-agent /bin/bash

### Add your credentials (provided you already made one with ssh-keygen)

    ssh-add ~/.ssh/id_rsa 

### if you want to list your credentials

    ssh-add -l

### Check your git settings

    cat .git/config

### After you made your new repo from github.com, put it here (If HTTPS)

    git add remote orgin https://github.com/username/repo.git

### Add the repo to your session (IF SSH)

    git remote add origin git@github.com:USERNAME/REPO.git

### If you typo, or add the wrong origin

    git remote rm origin

### Before commit, checks the file repo for all changes. 

    git commit -a

### But shit, you have to add a message somewhere in it. It doesn't tell you where, so just to do this. 

    git commit -m "A <50 word commit message"

### update your github repo with this

    git push -u origin master

### Force push if other one does not work.

    git push -f origin master
