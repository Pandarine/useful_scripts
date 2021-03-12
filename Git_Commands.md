`git init` - Create an empty Git repository or reinitialize an existing one.

`git add`: stage changes for the next commit. Add a change in the working tree to the index (staging area). This tells Git that you want to include updates to a particular file in the next commit. Subsequent changes to the file will not be reflected in the index until you add them, too. git add doesn't affect the repository itself - the changes are not actually recorded until git commit.

`git commit`: commit changes to the local repository. Store the current contents of the index in a new commit along with a log message describing the changes. (If you collaborate with other people, read the blog post How to write a good commit message).

`git status` - Useful command to view the state of working tree and staging area.

`git log` - Show commit history.

`git show` - Show one or more objects (blobs, trees, tags and commits).

`git diff` - Show changes between commits, commit and working tree, etc 

`git push` - push commits to the REMOTE repo

`git remote` — View remotes

<<<<<<< HEAD
* `git remote set-url origin https://.../…./` - Changes origin of the directory to specified repo (https://.../...)
=======
- `git remote set-url origin https://.../…./` - Changes origin of the directory to specified repo (https://.../...)
>>>>>>> fc69e4a7004efaa3f9c07031254b07e0d9973563

`git revert` - Add new commit that undoes the changes from a previous commit. This command adds new history to the project (it doesn't modify existing history).
	git revert commit_id — create new commit with the inverse of commit_id (default is HEAD).

# checkout #

`git checkout` - Change the state of working tree files, e.g. by switching branches or restoring files from a commit or from the index. The command takes content from the repository and puts it in your work tree. It doesn't make changes to the commit history.


* `git checkout branch-/commit-identifier filename` get a version of filename from branch tip of branch-name, or from commit-identifier

* `git checkout commit_id .` — restore working tree (all files) from given commit; last commit is HEAD

* `git checkout HEAD path/to/file` restore file path/to/file from HEAD commit

* `git checkout HEAD .` restore working tree (all files) from HEAD (last commit on current branch)

* `git checkout commit_id path/to/file` restore file from commit_id

* `git checkout commit_id .` restore working tree (all files) from commit_id; if you do `git status` after this, Git will compare the working tree to the HEAD commit and probably see a lot of changes

* `git checkout commit_id -- .` explicit syntax for `git checkout commit_id .` (`--` separates the branch/commit specifier from the path specifier, in case a branch and a file have the same name)

* `git checkout commit_id` switch to an un-named branch based on given commit → detached HEAD. If you do `git status` now, Git will compare the working tree to the detached HEAD commit and see no changes (https://stackoverflow.com/a/26399781/)


**Restore from INDEX (without branch/commit specifier, but with path specifier)**

* `git checkout -- path/to/file` restore file from INDEX (the absence of a branch/commit-specifier specifies the index)

* `git checkout -- .` restore working tree (all files) from INDEX (discard all unstaged changes)

* `git checkout .` abbreviation for the explicit syntax `git checkout -- .`

**Switch branches**

* `git checkout main` switch to the main branch


**Restore a revision in a new local branch**

* `git checkout -b testing commit_id` create a new branch ("testing") from commit_id; this is safer than `reset`

# reset #

`git reset` - Reset current HEAD to the specified state. This command modifies the index, or it changes which commit a branch head is currently pointing at. It may alter existing history (by changing the commit that a branch references).


* `git reset --soft HEAD~1` drop last commit, retain index and working tree	

* `git reset --soft A` index and working tree will NOT be altered (remain at state C; this is the safest option)

* `git reset --mixed A` (default) — also change the index; working tree remains at state C

* `git reset --hard A` also change index and working tree; you will go back to the state of A completely

The dropped commit is not immediately deleted; if you made a mistake, `git reflog` can help to locate and "restore" it


&nbsp;


`git branch` - List, create, or delete branches

* `git branch testing` create new branch (called "testing") at current commit

* `git branch` list local branches


`git merge` - Join two or more branches together, by creating a new commit. 


