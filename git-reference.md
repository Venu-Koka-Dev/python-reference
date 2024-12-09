# Index
1. Setup
2. 

# I. Setup
1. Download Git software from the official website : git-scm.com
2. Run the installer wizard
3. To check if Git is installed :
$ git --version

4. Create a working directory : python-learning

5. Initialize it to be a Git repository :
$ cd python-learning 
$ git init

6. One time configuration of the User's identity & initial branch 
$ git config --global user.name "Venu Koka"
$ git config --global user.email venu.kokaz@gmail.com
$ git config --global init.defaultBranch main

$ git config user.name
$ git config user.email
$ git config --list

7. You can take a local directory that is currently not under version control, and turn it into a Git repository
$ git init

8. Staging the changes that we have done (Untracked state to Staged state)
$ git add first.py

9. To commit to a repository -  At this point, you have a Git repository with tracked files and an initial commit.
$ git commit -m "Added a new file - first.py"

(Optional) If you want to bypass staging and directly commit all changes, you can use:
$ git commit -am "Your commit message"

10. To check the status of the git repo
$ git status

11. 


