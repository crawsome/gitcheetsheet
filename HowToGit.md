## Disclaimer
This is not an inclusive guide. This is my guide that I use to push my stuff up from other PCs. If it helps you, great!

## Quick Setup

1. install Git

    ```sudo apt-get install git```

2. configure Git 

    ```git config --global user.name "github_username"```

    ```git config --global user.email "youremail@email.com"```

3. Browse to chosen directory run this command.

    ```git init```

* If there's files in there already, just run this. **Note the capital A for "All".**

    ```git add -A```
    
* Use this command any time to check your git settings

    ```cat .git/config```

4. Be nice and make a README 

* Write some stuff in it. It's in markdown (.md) format, like this doc you're reading. 

    ```nano README.md```

* Nifty command to just make a local readme with some contents. 

    ```printf #PROJECTNAME\n Repository for PROJECTNAME ##Description\nShort Description\n##How To Use > README.md```

5. After you made your new repo from github.com, put it here (If HTTPS)

    ```git remote add orgin https://github.com/username/repo.git```

6. Add the repo to your session (IF SSH)

    ```git remote add origin git@github.com:username/repo.git```

* If you typo, or add the wrong origin

    ```git remote rm origin```

7. Before commit, checks the file repo for all changes, and commits them. 

    ```git commit -a```

* But shit, you have to add a message somewhere in it. It doesn't tell you where, so just to do this. 

    ```git commit -m "A less-than-50-character commit message"```

8. Push your changes to your github repo with this

    ```git push -u origin master```

* Force push if other one does not work.

    ```git push -f origin master```
    
## SSH Stuff:

1. IS the SSH agent running?

    ```ps -e | grep [s]sh-agent``` 

* If not, start it

    ```ssh-agent /bin/bash```

2. Add your credentials (provided you already made one with ssh-keygen)

    ```ssh-add ~/.ssh/id_rsa``` 

* If you want to list your local credentials

    ```ssh-add -l```
