# Index
1. What is Version ?
2. Semantic Versioning 2.0
3. What is Version Control System ?
4. Popular version control systems
5. Git
6. GitHub
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Version
Ex. Microsoft Windows 98, 2000, 2001
Ex. Microsoft Windows XP, Vista 
Ex. Microsoft Windows 10, 11 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Semantic Versioning 2.0
Software name X.Y.Z
X : major
Y : minor
Z : patch/bug
alpha : a
beta : b
release candidate : rc

Benefits:
 - clear understanding of version compatibility

Ex. Python 3.13.1
Ex. Python 3.14.0a2

Python
 1. Latest release - learning @ local computer
 2. Stable release - production env
 3. Pre-releases - experimenting & learning @ local computer

Note: (PEP) Python Enhancement Proposal is a document specifying the features if Python language.
       PEP stands for Python Enhancement Proposal. It is a design document that provides information to the Python community or describes a new feature for Python, its processes, or its environment. 
       PEPs are used to propose, discuss, and document changes or enhancements to the Python language and standard library
       
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Git 
 - A version control system
 - A software 
 - Official website: https://git-scm.com/
 - Better than other SCM tools like :  Subversion, CVS, Perforce, and ClearCase

Step 1 : Install Git software on your computer by going to the official website for your specific OS
Step 2 : To check if Git is installed
git --version

Step 3 : Create a folder/dir & cd to that directory
Step 4 : Initialize it to make it a Git repository (repo) : This creates a .git folder in your project directory, marking it as a Git repository
git init

Note : A .git hidden folder is created. On deleting this folder manually we can uninitialise or make the git repo a normal folder

(Optional) To configure the initial branch name to use in all of your new repositories, which will suppress this warning:
git config --global init.defaultBranch <newbranchname>

(Optional) The rename a newly created branch:
git branch -m <newbranchname>

Step 5 : Create a new file called : one.py

Step 6 : To stage the changes
git add one.py
(or)
git add .

Step 7 : To commit changes from staging area to the repo
git commit -m "added a new file one.py"

(Optional) To list all local branches
git branch
(or)
(Optional) To list all local + remote branches
git branch -a



























