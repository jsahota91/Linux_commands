# Using SSH Keys for GitHub
SSH keys help identify yourself on Git without requiring username and password.
You have a public SSH key which gets shared with GitHub, and private key which gets stored on your computer. It's used to grant you access.

## Create Repo in GitHub
In repositories just create a new repository, in this instance I called it Linux_commands

## Creating SSH key pair in GitBash
- `mkdir .ssh` : Make a directory for the SSH key pair
- `cd ~/.ssh` : change into this directory
- `pwd` : Check you are in this directory
- `ssh-keygen -t rsa -b 4096 -C yourGitHubEmail.com` : This generates your SSH key pair
- `ls` : Running this command you will see your public and private key pairs
- `id_rsa` and `id_rsa.pub` : The public key-pair file ends in pub and private key pair doesn't end in pub.
- `cat id_rsa.pub` : Display the contents of the public key pair with cat

## Use SSH Key Pair in GitHub
- Copy the public key pair
- Login to GitHub.com and go to settings (located in RHS dropdown top corner)
- In Settings, go to side tab SSH keys
- Click **Add SSH key**, then enter a name for the key, and paste your key as well, click Add Key to follow.
- Enter GitHub password when prompted

## Git commands for push local repo to remote repo
- `mkdir name` : Create a local directory, I called it Linux commands
- `git init` : Initialise the git folder
- `nano README.md` : Add a read me file, enter some information. Then `ctrl x` and `ctrl y` and `enter` to save the file and exit
- `git add .` : Add any files in the folder to the local repo
- `git commit -m "message"` : Add a commit message
- `git branch -M main` : Create a branch for main
- `git remote add origin "remote repo url"` : Create a link to the remote repo
- `git push -u origin main`: pushes the changes of local directory to the remote repo
- `git push` : you can use this thereafter to push changes

