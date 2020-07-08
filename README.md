# Git-bash :-
# Installing Git :-
* To download Git:

		1.Go to https://git-scm.com/downloads
	
		2.download the software for Windows
	
		3.install Git choosing all the default options

# First Time Git Configuration:- 
* Sets up Git with your name:

		git config --global user.name "<Your-Full_Name>"
	
* Sets up Git with your email:	

		git config --global user.email "<your-email-address">
		
* Makes sure that Git output is colored:

		git congig --global color.ui auto
		
* Displays the original state in a conflict:
		
		git config --global merge.conflictstyle diff3
		
		git config --list
		
# Git & Code Editor:-
The last stop of configuration is to get Git working with your code editor. Below are three of the most popular code editors. If you use different editor.

* Atom Editor Setup

		git config --global core.editor "atom --wait"
		
* Sublime Text Setup

		git config --global core.editor "C:Program Files/Sublime Text 2/sublime_text.exe' -n -w"
		
* VSCode Setup

		git config --global core.editor "code --wait"
		
# Repository Commands
* git init
	
		* Create brand new repositorie(reps) on your computer.
	
* git clone

		* Copy existing repos from somewhere else to your local computer.
	
* git status

		* Check the status of a repo.
	
# Useful Commands
		1. ls - Used to list files and directories.
	
		2. mkdir - Used to create a new directory.
	
		3. cd - Used to change directories.
	
		4. rm- Used to remove files and directories.

