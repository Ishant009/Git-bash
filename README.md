# Git-bash :-
# Installing Git :-
* To download Git:

		1.Go to https://git-scm.com/downloads
	
		2.download the software for Windows
	
		3.install Git choosing all the default options

# First Time Git Configuration:- 
* Sets up Git with your name:

		>>git config --global user.name "<Your-Full_Name>"
	
* Sets up Git with your email:	

		>>git config --global user.email "<your-email-address">
		
* Makes sure that Git output is colored:

		>>git config --global color.ui auto
		
* Displays the original state in a conflict:
		
		>>git config --global merge.conflictstyle diff3
		
		>>git config --list
		
# Git & Code Editor:-
The last stop of configuration is to get Git working with your code editor. Below are three of the most popular code editors. If you use different editor.

* Atom Editor Setup

		>>git config --global core.editor "atom --wait"
		
* Sublime Text Setup

		>>git config --global core.editor "C:Program Files/Sublime Text 2/sublime_text.exe' -n -w"
		
* VSCode Setup

		>>git config --global core.editor "code --wait"
		
# Repository Commands

* Create brand new repositorie(reps) on your computer.
		
		>>git init
	
* Copy existing repos from somewhere else to your local computer.
		
		>>git clone <url>
	
* Check the status of a repo.
		
		>>git status
	
# Useful Commands
		1. ls - Used to list files and directories.
	
		2. mkdir - Used to create a new directory.
	
		3. cd - Used to change directories.
	
		4. rm- Used to remove files and directories.


# Review Repo History

* Displays information about the existing commits. 

	* It shows the SHA, the author, the date, the commit message.
	
			>>git log 


	* The git log --online show first 6 letter of SHA and the commit message.
		
			>>git log --oneline


	* Displays information about the given commit. The output of the git show command is exactly the same as the git log -p command.
		
			>>git show
		
* View Files Changes

	* This command is used to display the files that have been changed in the commmit as well as the number of lines that have been added or deleted.

			>>git log --stat

	* The git log command has a flag that can be used to display the actual changes made to a file

			>>git log -p

	* The git show command will show only one commit.

			>>git show <sha id>
		
# Add Commits to a repo.
 
 * Add files from the workng direcotry to the staging index.
	
	* Add all files
	
			>>git add .
	
	* Add specific files
	
			>>git add <filename>,<filename>

* This command will not distroy the work but it just removes it from the Staging index.

			>>git rm --cached <filename>
		
* Take files from the staging index and save them in the repository.
	
	* Commit files
		
			>>git commit
	
	* Commit the repo with message.
		
			>>git commit -m "Initial commit"  



* Displays the difference between two version of commits.

		>>git diff

# Tagging, Branching and Merging

* Tagging
	
	* Git allow to put tag on various commit.

		* Add tags to specific commits
	
				>>git tag -a v1.0
			
		* A Git tag can be deleted with the -d flag (for delete!) 
	
				>>git tag -d v1.0
	
		* To show  all existing tag
			
				>>git tag 

* Branching 

	* Git branch Allow multiple lines of development

	* It can be use to 
	
		* List all branch name in the repository
		
				>>git branch 
	
		* Create new branch 
			
				>>git branch <branchname>
		
		* Create new branch from existing commit>
			
				>>git branch <branchname> <sha-id of existing branch>
		* Delete branch 
			
				>>git branch -d <branchname>

	* Checkout is used to change the branch from one to another. 
	
			>>git checkout <branchname>

* Merging 

	* Combine the differnce of different branches.
	
			>>git merge  <name-of-branch-to-merge-in>

	
* Merge Conflict 

	The editor has the following merge conflict indicators:

		<<<<<<< HEAD everything below this line (until the next indicator) shows you what's on the current branch.
	
		||||||| merged common ancestors everything below this line (until the next indicator) shows you what the original lines were.

		======= is the end of the original lines, everything that follows (until the next indicator) is what's on the branch that's being merged in.

		>>>>>>> heading-update is the ending indicator of what's on the branch that's being merged in (in this case, the heading-update branch)
		Resolving A Merge Conflict.

	 Git is using the merge conflict indicators to show you what lines caused the merge conflict on the two different branches as well as what the original line used to have. So to resolve a merge conflict, you need to:

		1. Choose which line(s) to keep.

		2. Remove all lines with indicators.


# Undoing changes

* Changing the most recent commit-

		>>git commit --amend 

* Reverse given commint given with sha-

		>>git revert <sha of commit to revert>

* Erases(reset) commits
		
		>>git reset <reference-to-commit>
		
		>> git reset --soft HEAD^

	
* Git Reset's Flags
	
	The way that Git determines if it erases, stages previously committed changes, or unstages previously committed changes is by the flag that's used. The flags are:

	--mixed take the changes made in commit and move them to the working directory

	--soft  the changes moved to the Staging Index

	--hard  The changes are complete erased
	
* Backup Branch
	
		>>git branch backup


