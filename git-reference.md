# Index
1. Setup
2. Commonly used commands locally
3. Branching
4. Remotes
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
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

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## II. Commonly used commands locally  
7. You can take a local directory that is currently not under version control, and turn it into a Git repository
$ git init

8. Staging the changes that we have done (Untracked state to Staged state)
$ git add first.py

(Optional) To revert back the staging step
$ git restore --staged <file>...

10. To commit to a repository -  At this point, you have a Git repository with tracked files and an initial commit.
$ git commit -m "Added a new file - first.py"

(Optional) If you want to bypass staging and directly commit all changes, you can use:
$ git commit -am "Your commit message"

10. To check the status of the git repo
$ git status

11. TO check the commit points on a branch
$ git log   

12. To checkout a particular commit point 
$ git checkout 6d04d01b6e1309513dc17a82a1eaa6edd3f41397
Note: switching to '6d04d01b6e1309513dc17a82a1eaa6edd3f41397'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6d04d01 Added a new file - first.py

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## III. Branching
13. Create a new branch
    
