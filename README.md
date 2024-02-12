# GIT-Tutorial
## Repository 
### Creating a Repository 
__Repository__: A repository is a collection of files of various versions of a Project
* Create a folder for your project on the local hard drive and name it as needed 
* Use __cd__ to change the directory to the folder you created 
* Type in __git init__ to initialize a new Git repository in the current repository you are in 
### Checking the Status of the Repository
* Use git status to examine/check the current status of the repository 
* With the new repository the output should be:

On branch master 

No commits yet 

nothing added to commit (use __git add__ to track)
* __git add <file>__ will add a specific file to the staging area
* __git add__ will add all modified and new files to the staging area

### Cloning a Repository → having a local copy of the repository 
1. Go to GitHub.com
2. Click the green dropdown button where it says “<> Code”
3. Copy URL
4. Use __git clone__ ___insert URL___ 

### Working Tree 
* The working tree tracks the files, folders, and the changes that are made inside the .git folder
  * Use __ls__ to check the current repository/directory contents, giving you a list of files/folders. Since this is a new repo, there will be nothing there
  * You can also use __ls -a__ in order to show all the files, including the hidden ones
  * You can use __touch__ ___filename___ to create a new file in the repo. Note that the files in your repository folder are the working tree
* Stages in the working tree:
  * __Untracked__: the Git repo is not able to track the file; the file is never staged nor committed
  * __Tracked__: the Git repo is able to track the file; the file is committed but not staged in the working directory
  * __Staged__: the file is ready to be committed and placed in the staging area 

### Remote Repository:  versions of your project that can be accessed through the internet or network; repo stored on GitHub, not on your computer 
Commands to create remote repo:
* __git remote add origin <your_repository_URL>__
* __git branch -M main__
* __git push -u origin main__

### Branch: allows you to work on separate things until everything needs to be merged together 
* __git branch__ will list out all of the branches in the repository 
* __git branch <branch_name>__ will create a new branch 

### Stash: stashes the changes in the staging area, thus allowing you to switch to different branches or commits without fully committing
* __git stash__
* __git stash pop__ allows you to release any stashes you saved so that you could pull any recent changes 

#### Commit graph: represents all the data 
* By using __git graph__ it allows you to view all of the history in the repo. The history consists of ___nodes___ which show each individual commit that was pushed. These commits have a unique ___hash___. A hash is a hexadecimal string that contains 40 characters but usually in the git graph, will only show the first 7

### Commit: saving any changes that were made the history; it will keep track of what changes were made by who and when 
* Use__git commit -m__ to create a new commit with changes along with a message with description of changes made 

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


