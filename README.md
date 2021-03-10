# useful_scripts

git init - Create an empty Git repository or reinitialize an existing one.


git add: stage changes for the next commit. Add a change in the working tree to the index (staging area).


git commit: commit changes to the local repository. git commit -m "fixed two bugs and changed output format"


git status - Useful command to view the state of working tree and staging area. 

git log - Show commit history.

git show - Show one or more objects (blobs, trees, tags and commits).

git diff - Show changes between commits, commit and working tree, etc

git diff  # Changes WORKING TREE -> INDEX
git diff --cached  # Changes INDEX -> LAST COMMIT; what you would be committing if you run "git commit"
git diff HEAD  # Changes WORKING TREE -> LAST COMMIT; what you would be committing if you run "git commit -a"
git diff HEAD~1  # Changes WORKING TREE -> SECOND LAST COMMIT
git diff HEAD~1 HEAD  # Changes SECOND LAST COMMIT -> LAST COMMIT
git diff --stat  # Summarize changes (filenames and amount of changes)


git add - select changes (store them to the INDEX)
git commit - record changes LOCALLY (store them as COMMITS)
git push - push commits to the REMOTE repo 


git remote — View remotes
git remote -v — Be more verbose and show remote URL after name


git revert - Add new commit that undoes the changes from a previous commit. This command adds new history to the project (it doesn't modify existing history).

git checkout - Change the state of working tree files, e.g. by switching branches or restoring files from a commit or from the index. The command takes content from the repository and puts it in your work tree. It doesn't make changes to the commit history.

git reset - Reset current HEAD to the specified state. This command modifies the index, or it changes which commit a branch head is currently pointing at. It may alter existing history (by changing the commit that a branch references).

git checkout behaves differently depending on how you use it. Essential examples are very helpful. The syntax includes a branch/commit specifier and a path specifier:


