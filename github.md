# About

Manual page for GitHub

# Logging

Show git insight network of the branches:
- `git log --graph --oneline --all`

Show code recent changes on log:
- `git log -p`

Show git log based on the author
- `git log -p --author=someUser`

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

List all branches exist on remote repo.
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
