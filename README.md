# github_tutorial

---
## PROMPT COMMANDS

### Windows Commands
| Command | Description |
| :------ | :---------- |
| dir |  Lists all files and folders within the  directory you're in. |
| cd | Changes the directory you're in. |
| cd .. | Allows user to go up in the directory hierarchy. |
| help | Lists commands within the help utility.  Note: incomplete listing.

### Git Bash Commands
| Command | Description |
| :------ | :-----------|
| git status | Compares your file versions with GitHub's in a detailed overview.
| git add | Stages changes we've made.
| git commit -m "comment" | This commits changes that have been added/staged, where the comment is published.
| git push | This syncs our committed changes with GitHub.
| git pull | This pulls the latest version of the repository [branch] from GitHub.
| git clone <url> | Places a repository clone [copy] on your computer.
| git branch [name_of_new_branch] | Creates a new branch.
| git checkout [branch_name] | Switches to specified branch.
| help | Lists commands within the help utility.  Note: incomplete listing.

Note: **git pull** executes a **git fetch** followed by a **git merge** to update the local repository with the contents of the remote repository.


### Windows Command Prompt vs Git Bash
Git commands can be executed via either Git Bash or the Windows Command Prompt.  
However, Git Bash specifies which branch you're working within, which is a necessity.

---

##WORKING WITH A NEW REPOSITORY [Windows]

### Repository Creation
A repository can be created within GitHub and is straightforward with the user interface.

### Creating a CLONE of the REPOSITORY on your computer
In order to use the Git Bash command prompt, create a clone of the new repository on your computer.

1. Open and use the Windows command prompt:

   *cmd*

2. Navigate to the desired destination/folder on your computer for the repository

   *cd*

3. Now enter within the Windows Command Prompt:

   *git clone URL*  where the URL is found on the webpage for the GitHub repository.

   The repository now exists in the location specified in step 2.

---

##PUSHING CHANGES FROM YOUR COMPUTER TO GITHUB
After making a change to the repository on your computer you'll need to push the change to GitHub, i.e. sync up with <GitHub.com> to update changes.

1. Check the status of the repository, i.e., view changes that have been made

   *git status*

2. Stage the changes made

   *git add*

   if you add -A at the end of the line then all changes will be staged.

3. Commit changes

   *git commit -m "comment"*

   where the comment field is important because it's used to identify the overall change made

   if no comment field is completed then on the resultant screen hit escape and enter in the command line *:wq*

4. Push changes, i.e., sync up with GitHub and promulgate changes there

   *git push*

---

##RECCOMENDATION
Use a text editor which can interface with GitHub repositories, such as [Atom](atom.io).
