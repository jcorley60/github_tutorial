# github_tutorial
---

## PROMPT COMMANDS


### Windows Commands
| Command | Description |
| :------ | :---------- |
| dir |  Lists all files and folders within the  directory you're in. |
| cd [directory_name]| Changes the directory you're in. |
| cd .. | Allows user to go up in the directory hierarchy. |


### Git Bash Commands
| Command | Description |
| :------ | :-----------|
| pwd | Prints the Present Working Directory.
| ls | Lists all files and folders within the  directory you're in.
| git status | Compares your file versions with GitHub's in a detailed overview.
| git diff | 'Difference'. Displays differences between your active repository and GitHub's. Not recommended. Use GitHub instead.
| git add | Stages changes made.
| git commit -m "comment" | This commits changes that have been added/staged, where the comment list string is published.
| git push | This syncs our committed changes with the GitHub repository.
| git pull | This pulls the latest version of the repository [branch] from GitHub.
| git clone <url> | Places a repository clone [copy] on your computer.
| git branch [name_of_new_branch] | Creates a new branch.
| git checkout [branch_name] | Switches to specified branch.


Note: **git pull** executes a **git fetch** followed by a **git merge** to update the local repository with the contents of the remote repository.


### Windows Command Prompt vs Git Bash
Git commands can be executed via either Git Bash or the Windows Command Prompt.  
However, Git Bash specifies which branch you're working within, which is a necessity.


---


## WORKING WITH A NEW REPOSITORY [Windows]

### Repository Creation
A repository can be created within GitHub and is straightforward with the user interface.

### Creating a CLONE of the REPOSITORY on your computer
In order to use the Git Bash command prompt, create a clone of the new repository on your computer.

1. Open and use the Windows command prompt:

   **cmd**


2. Navigate to the desired destination/folder on your computer for the repository

   **cd**


3. Now enter, within the Windows Command Prompt:

   **git clone URL**  where the URL is found on the webpage for the GitHub repository.

   The repository now exists in the location specified in step 2.


---


## PUSHING CHANGES FROM YOUR COMPUTER TO GITHUB
After making a change to the repository on your computer you'll need to push the change to GitHub, i.e. sync up with <GitHub.com> to update changes.

1. Check the status of the repository, i.e., view changes that have been made

   **git status**


2. Stage the changes made

   **git add [-A or filename]**

   if you add -A (capitalized) at the end of the line then all changes will be staged. e.g. **git add -a**.  Otherwise the file where changes have been made can specified by filename.


3. Commit changes

   **git commit -m "comment"**

   where the comment list string is important because it's used to identify the overall change made

   if no comment string is provided then on the resultant prompt screen hit escape and enter in the command line **:wq**


4. Push changes, i.e., syncs up with GitHub and promulgates changes there

   **git push**


---

## Pull Requests
Pull requests make full use of Git for its intended use as a Version Control System, where a team of people are contributing simultaneously. For multiple users to work on the same repository simultaneously, branches are needed.

1. Create a new branch (off of the master branch).  This new branch is a complete copy of the master branch.

   **git branch [branch_name]**

   Double-check w/ **git branch** which lists all available branches.  The branch we're currently in is denoted with an asterisk.

2. Specify an upstream branch for branch pushes.  This specified branch will be placed upstream of your branch.

   **git push --set-upstream origin [master, etc.]**
   or to unset the upstream branch:
   **git branch --unset-upstream [master, etc.]**

3. Switch over to the new branch
   **git checkout [branch_name]**
   or
   **git checkout -b [branch_name]** would create the new branch and then immediately switch over to it.

4. Make changes and then commit changes on your new branch.

   **git push origin [branch_name or master]**

   *Note:* If you don't commit existing changes then Git won't let you switch branches.

5. Merge new code with master branch.
   **git merge origin/[branch_name]**

6. Push changes to the master branch
   **git push origin master**

---

## Creating an SSH Key
[SSH Keys](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
SSH Keys identify the user who's interacting with the Git remote repository.  Creating an SSH Key obviates the need to supply a password every time a change is made.  The GitHub Desktop app can also be used for this purpose, although it runs SSL by default.

---

## RECCOMENDATION
Use a text editor which can interface with GitHub repositories, such as [Atom](https://atom.io).
