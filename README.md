# GIT-Tutorial
## Introduction
Git is a version control system that is used by many Computer Science students and developers that manage and track changes in projects. Git is essential for efficient collaboration and project management. In this tutorial, we will be covering some of the basics of Git with examples to help get you started 

## Installing Git 
Before you can start using Git, you need to make sure that you have it installed in your system. It is available for Windows, macOS, and Linux. Download the installer for your operaitng system from the Git wesbite [https://git-scm.com/downloads](https://git-scm.com/downloads)

To check to see if it has installed, open your terminal, command prompt, or GitBash and run the command:
```
git --version
```
<img width="167" alt="git version" src="https://github.com/PhilyciaP/GIT-Tutorial/assets/94141468/88a0cbc5-d8ce-4a55-a04d-90018f076b79">

## Configuring Git
After installing Git, you will need to configure it with some information such as your name and email. Run the commands:
```
git config --global user.name "Your Name"
git config --globel user.email "your@email.com"
```
In this case, make sure to insert your actual name and email into the quotation marks.

<img width="284" alt="git config" src="https://github.com/PhilyciaP/GIT-Tutorial/assets/94141468/cd78935d-8ac4-45a7-9542-1a722224395e">

## Repository 
### Creating a Repository 
A Git __repository__ (or repo) is a collection of files of various versions of a Project. Create a folder for your project on the local hard drive and name it as needed. We will start by creating a new directory to which you can use the command ```mkdir```. Use ```cd``` to change the directory to the folder you created. To initialize a new Git repository in the current repository you are in, type in ```git init```. It should look something like:

<img width="376" alt="repo example" src="https://github.com/PhilyciaP/GIT-Tutorial/assets/94141468/b41b579d-53bf-4998-9cdd-c9c8849047e7">

### Cloning a Repository
Cloning a repository allows you to bring remote repositories onto your local machine, enabling you to work on projects, collaborate with others, and maintain backups of important codebases. 
First, find the URL of the repository that you want to clone from Github. Then, type:
```
git clone https://github.com/paste_URL_here/directoryName
```

### Creating and Keeping Track Files
To check what files are in your repository, you can use the command __ls__
To create a new file, you are going to use the command:
```
touch filename.txt
```
To add the new file into the repository, use the command:
```
git add filename.txt
```
If you want to create a simple text file and edit in the terminal, command prompt, or Gitbash, you can use the command:
```
echo "type message here" > filename.txt
```
In this case, to open this text file, you are going to use the command:
```
start filename.txt
```
<img width="365" alt="git files" src="https://github.com/PhilyciaP/GIT-Tutorial/assets/94141468/921589c1-4b11-4605-a056-600cd1d100ec">

### Commit and Commit Graph 
To __commit__ allows you to savie any changes that were made the history and it will keep track of what changes were made by who and when. It also allows you to keep track of the changes you made by adding a description of said change. 
To commit to your repository, use the command:
```
git commit -m "insert message here"
```
The __commit graph__ represents all the data and allows you to view all of the history in the repo. The history consists of ___nodes___ which show each individual commit that was pushed. These commits have a unique ___hash___. A hash is a hexadecimal string that contains 40 characters but usually in the git graph, will only show the first 7. 
To use this command, run:
```
git log
```
![Screenshot 2024-04-23 073613](https://github.com/PhilyciaP/GIT-Tutorial/assets/94141468/dc935d8c-086a-4b81-ad99-7d55869ed026)


### Branching
__Branching__ allows you to work on separate things until everything needs to be merged together. It also allows you to make specific changes without affecting the __master branch__.
To list out all of the branches in your repository, run:
```
git branch
```
To create a new branch, use the command:
```
git branch branch_name
```
To switch branches, run:
```
git checkout branch_name
```
![git branch](https://github.com/PhilyciaP/GIT-Tutorial/assets/94141468/41a33275-5d2f-4ea3-95ce-2774e44fa04d)

### Merge 
After you are done making changes in that branch and are ready to combine those changes to the master branch, you are going to use __git checkout master__ to switch back to the master branch. Once you are back in the master branch, you are going to __merge__ the branch by running the command:
```
git merge branch_name
```


### Stash 
To __stash__ allows you to save and switch to another task without having to fully commit your changes if you are not ready. Run the command:
```
git stash
```
If you want to continue working on the task you have stashed, use the command:
```
git stash pop
```


### Push
To __push__ means to ___upload___ any changes that you made to repository to the servers and in this case, you are uploading to Github. There are a few steps to do this process:

  1. Create a remote repository on Github and copy the URL
  2. Link repository to your computer
```
git remote add origin <paste_repository_URL>
```
  3. Push commits to Github
```
git push -u origin main
```
__Note:__ The command in Step 3 is telling Git to link your local master to the remote main, to which you will only need to do that step once. Afterwards, you can simply use the command:
```
git push
```

### Pull
__Pulling__ allows you to take changes from others to keep the repository up to date. You are ___downloading___ the changes to the server. To fetch the changes from the remote repository and merge with the current branch, use the command:
```
git pull
```

## Congratulations!
You have finished through the tutorial! We covered some of the basic commands of Git and hopefully you were able to follow along. By practicing these commands with each project you create and collab with others, it will become part of your muscle memory. Enjoy Git!

