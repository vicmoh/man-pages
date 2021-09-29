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

# Find running port and kill

Find out the process ID (PID) which is occupying the port number (e.g., 4000) you would like to free

```
sudo lsof -i :4000
```

Kill the process which is currently using the port using its PID

```
sudo kill -9 PID
```
