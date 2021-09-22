# About

This file contain manual page for
`pip Installs Packages`.

# Virtual environment

Allow run permission

```
chmod 755 ./file
```

Upgrade

```
sudo pip install --upgrade requests
```

Create virtual environment

```
virtualenv env
```

Install requirement files using `venv`.

```
venv env/bin/pip install -r requirements.txt
```

# Managing packages

Uninstall all packages

```
pip3 freeze | xargs pip3 uninstall -y
```
