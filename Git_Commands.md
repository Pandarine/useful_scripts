git init - Create an empty Git repository or reinitialize an existing one.

git add: stage changes for the next commit. Add a change in the working tree to the index (staging area). This tells Git that you want to include updates to a particular file in the next commit. Subsequent changes to the file will not be reflected in the index until you add them, too. git add doesn't affect the repository itself - the changes are not actually recorded until git commit.

git commit: commit changes to the local repository. Store the current contents of the index in a new commit along with a log message describing the changes. (If you collaborate with other people, read the blog post How to write a good commit message).


git status - Useful command to view the state of working tree and staging area.

git log - Show commit history.
git show - Show one or more objects (blobs, trees, tags and commits).

