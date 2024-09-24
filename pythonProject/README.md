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
3. Run `git diff <hash-id1> <hash-id2>
4. Alternatively, to check the difference between the most recent and previous commit run `git diff HEAD^ HEAD`

Use `git checkout` to point to the previous commit and then back to the most recent commit.
1. Find each commits id.
2. To point to another commit run `git checkout <hash-id>` (run the command for both commits)

Restore a specific file to its state in a previous commit
1. Find the commit id of the state where the file should be restored to.
2. Run `git checkout <hash-id> -- <file-name>`
3. Note: The file now should be at a staged state, commit the file!
