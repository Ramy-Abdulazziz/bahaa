# Basic Git Commands
A repository to practice basic git commands
# Git On Mac

Usually a basic wrapper for Git is preinstalled on MacBooks, check if you have it pre installed by using in the terminal: 


```
git --version
```

if you get a version number you can move on, if you get a prompt such as : 

```
The git command requires the command developer tooks. Would you like to install the tools now?
```

You need to click install and this will install git. Use the above command to confirm installation. 

# Windows

Windows does not come with Git pre installed as its not based on UNIX, but you can download [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) for windows (windows subsystem for linux), which will have it pre installed. Download an Ubuntu image if you go this route, it should be the default when you run : 

```

wsl --install
```

if you run into issues follow the guide or let me know. Once you have it set up generate your ssh key within WSL (run all the commands in the guide below in your wsl terminal, not cmd or powershell). Within WSL you will be within the Linux filesystem to access your local machine you can cd into it: 

```
cd /mnt/c
```

then you will be in your C drive (if you use a different letter drive just use that instead of C). 

# How To Clone A Repository 

You should a green "code button" towards the right of the screen - click this and you should see an option for SSH, copy this key. You will need to have your [SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) key generated for this to work.

## Navigating to a directory

In your terminal navigate to the location you want to clone this directory into, to navigate to a directory or location in your system use the cd command: 


```
cd /path/to/your/directory
```

You can make a new directory of file using the mkdir command: 

```
mkdir name_of_your_directory
```

## Cloning

Cloning means downloading a copy of the code you see online on your local machine, to do this when you are in your desired directory run the command: 

```
git clone shh-key-you-copied
```

# Pulling A Repository

While working with others there may have been changes made to the code base that you want to make sure you also have on your local machine. Every time you work you will want to do a "pull" which means that you download the latest changes. Navigate to the directory that holds your repository and use the command: 

```
git pull
```

# Pushing To A Directory

After making changes you want to "push" them back to github so that all others working with you can also pull down your new changes, to do this we make a commit and push. Commiting is essentially specifying which files you want to push to github, to do this you use to add, commit, and push commands. First you commit your changes. 

```
git add file_you_want_to_add
```

if you are in a directory that has changes and you want to add them all to the same commit you can also use the shorthand: 

```
git add .
```

Once you added your files you must commit them, and add a message: 

```
git commit -m "a short explanation of what you did"
```


After commiting push your changes back to GitHub: 

```
git push
```

You will be asked for your password if you created one for your ssh key. You should then see a message showing that you successfully pushed. 





