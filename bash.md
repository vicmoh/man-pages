# About

Manual page of bash and terminal
commands. 

# Find command

Search file
- `find ./folder -iname "*.js"`

Delete all files in folders and subfolders
- `find . -name "*.bak" -type f -delete`

Show files, use this for precaution before deleting
- `find . -name "*.bak" -type f`

# Grep command

Search text in files in ignore case.
- `grep -ri theText ./folder`
