# Task: Learn Git - Stage 1

Check you have git on your machine `git --version`

Create your first Git repo named 'tech264-test-git'
1. Create 'tech264-test-git' folder as usual.
2. Open a terminal and change directories to point to the folder,
3. Run the command to initiate a git repo `git init`

Create a README.md file via the IDE

Do your first commit
1. Run `git status` to confirm the added file is in a modified stage.
2. Stage the file by running `git add .` (adding the . stages all unstaged files).
3. Make commit and associate it with a message `git commit -m "My first commit"`
4. Run `git status` to confirm repo state.

Make changes to README.md file and do another commit.
* Edit file and follow 'Do your first commit' steps.

Check differences between commits
1. Run `git log` to display the logging info for both commits.
2. Find the hash id associated with each commit log.
3. Run `git diff <hash-id1> <hash-id2>`
4. Alternatively, to check the difference between the most recent and previous commit run `git diff HEAD^ HEAD`

Use `git checkout` to point to the previous commit and then back to the most recent commit.
1. Find each commits id.
2. To point to another commit run `git checkout <hash-id>` (run the command for both commits)

Restore a specific file to its state in a previous commit
1. Find the commit id of the state where the file should be restored to.
2. Run `git checkout <hash-id> -- <file-name>` or `git checkout HEAD~1 -- <file-name>`
3. Note: The file now should be at a staged state, commit the file!

# Task: Learn GitHub - Stage 2

Given that we have created an account on GitHub we can follow the below steps to set up our online repo:

1. Create a new repository.
2. Give it a name - if attempting to copy a local repo to this online repo give it the same name as the local repo.
3. Ensure it is Public if wanting others to have access or Private for private usage
4. Confirm creation

Set up by creating a new repository on the command line

* `git init` Initialise repository.
* `git branch -M main` Rename standard master branch to main.
* `git remote add origin https://github.com/AdonisAlgos/ONLINE_REPO_NAME`
* `git push -u origin main`

Set up by pushing an existing repository from the command line

* `git remote add origin https://github.com/AdonisAlgos/ONLINE_REPO_NAME`
* `git branch -M main`
* `git push -u origin main`

What are some things we want to ignore?

* Sensitive (passwords, etc) personal files
* Large files/folders that don't need to be pushed
* Build folders (/bin, /out, etc)

To do this we can create a .gitignore file and define file/folder names that from that point onwards will
prevent git from tracking these files/folders.

**IMPORTANT!** 
To achieve this, we can create a .gitignore file and specify the file or folder names that should be ignored. 
From that point forward, Git will stop tracking the specified files or folders.

**IMPORTANT!**
If the file or folder has been previously been commited it can be removed by running ` git rm --cached  -r <file_or_folder_name>`

**IMPORTANT**
If the file or folder is still accessible in previous versions we can action as follows:

Option 1: 
* Remove previous commits with that file. (e.g. use 'git reset' DANGEROUS)

Option 2: 
1. Remove GitHub repo (Now safe!).
2. Remove sensitive information from your local file.
3. Remove .git folder from your local repo.


