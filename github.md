# About

Manual page for GitHub

# Undo commit

- Do `git reset HEAD^` for as many commits you want to undo, it will keep your changes and your actual state of your files, just flushing the commits of them.

# Logging

Show git insight network of the branches:
- `git log --graph --oneline --all`

Show code recent changes on log:
- `git log -p`

Show git log based on the author
- `git log -p --author=someUser`

# Merging

To abort the merge
- `git merge --abort`

Viewing list of merge conflict files
- `git diff --check`

# Push and reset

Make sure everything is pushed up to your remote repository (GitHub):
- `git checkout master`

Overwrite "master" with "better_branch":
- `git reset --hard better_branch`

Force the push to your remote repository:
- `git push -f origin master`

Remove the files where files are left behind when git reset happen:
- `git clean -f -d`

Ref: <https://stackoverflow.com/questions/2763006/make-the-current-git-branch-a-master-branch> 

# Removing file and ignore

Create `.gitignore` file for ignoring to git.
- .gitignore
- simply add `**/.DS_Store`: to ignore that files.

Remove all files in gitignore:
- git rm --cached `git ls-files -i --exclude-from=.gitignore`

If is `.DS_Store` is in the git repo, command below removes them.
- `find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch`
- git commit and push once done.

Show what will be removing from .gitignore:
- `git clean -xdn` 
To remove all that is shown:
- `git clean -xdn`

Remove the cached gits.
If you can't remove the files in `.gitignore`:
- `git rm -r --cached .`

# Branches

To show local branches:
- `git branch -a`

Refresh branch list:
- `git remote update origin --prune`

List all branches exist on remote repo:
- `git branch -r`

Delete remote branch:
- `git push origin --delete <branch_name>`
- `git push <remote_name> --delete <branch_name>`

Delete local branch:
- `git branch -D <branch_name>`

Revert the changes:
- `git stash`

- Revert to head
git reset --hard remotes/origin/HEAD

# Git sub-modules

Update submodule:
- `git submodule update --init --recursive`

Add git sub-module in `.gitmodules` index:
- `git submodule add <url> <package-path>`

Remove git sub-module in `.gitmodules` index:
- `git rm --cached <package-path>`

Pulling all sub-modules:
- `git pull --recurse-submodules`

Cloning repo with it's git module:
- `git clone --recursive [URL to Git repo]`

To load sub-module:
- `git submodule update --init --recursive`

Executing a command on every sub-module:
- Ex. `git submodule foreach --recursive 'git reset --hard'`

Create a file name `.gitmodules` in work dir.
The file will be format:
```
[submodule "libfoo"]
	path = include/foo
	url = git://foo.com/git/lib.git

[submodule "libbar"]
	path = include/bar
	url = git://bar.com/git/lib.git
```

# Warnings and errors.

If you get error: cannot lock
- `git gc --prune=now`
