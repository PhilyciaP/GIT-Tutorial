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
saving any changes that were made the history; it will keep track of what changes were made by who and when 
* Use__git commit -m__ to create a new commit with changes along with a message with description of changes made
#### Commit graph: '
represents all the data 
* By using __git graph__ it allows you to view all of the history in the repo. The history consists of ___nodes___ which show each individual commit that was pushed. These commits have a unique ___hash___. A hash is a hexadecimal string that contains 40 characters but usually in the git graph, will only show the first 7


### Branch: allows you to work on separate things until everything needs to be merged together 
* __git branch__ will list out all of the branches in the repository 
* __git branch <branch_name>__ will create a new branch 

### Stash: stashes the changes in the staging area, thus allowing you to switch to different branches or commits without fully committing
* __git stash__
* __git stash pop__ allows you to release any stashes you saved so that you could pull any recent changes 

#### Commit graph: represents all the data 
* By using __git graph__ it allows you to view all of the history in the repo. The history consists of ___nodes___ which show each individual commit that was pushed. These commits have a unique ___hash___. A hash is a hexadecimal string that contains 40 characters but usually in the git graph, will only show the first 7



### Push: pushing changes that you made to repository; uploading changes to the servers 
* __git push__ pushes commits to the remote repository
* __git push <remote>__ pushes commits to a specified remote repository
* __git push <remote> <branch>__ pushes commits to a specified branch in the remote repository

### Pull: pulling changes from others to keep the repository up to date; downloading the changes to the server 
* __git pull__ fetches changes from remote repository and merges with current branch 
* __git pull <remote>__ fetches changes from a specified remote repository and merges with current branch

### Rebase: taking the commits of one branch and “replaying” it on a different branch (end of the branch). The resulting commit graph will be a singular line; the history is linear. 
* __git pull --rebase__ will fetch the changes from the remote repository and rebases the current branch with the updated branch 

If a merging conflict occurs while rebasing, it will stop and ask to fix each conflict one at a time to which you would then type:
* __git add <resolved file>__
* __git rebase --continue__

If the error still occurs, you could also use __git rebase --abort__ which will bring you back to the beginning before the rebase 


