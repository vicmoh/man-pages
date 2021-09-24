# About

This file contain manual page for
`pip Installs Packages`.

# Virtual environment

Create virtual environment.

```
virtualenv env
```

Allow run permission and run environment.

```
cd ./env/bin
chmod 755 ./activate
source ./activate
```

Upgrade

```
sudo pip install --upgrade requests
```

Install requirement files using `venv`.

```
venv env/bin/pip install -r requirements.txt
```

# Requirements

Creating requirements

```
pip freeze > requirements.txt
```

Install from requirements

```
pip install -r /path/to/requirements.txt
```

# Managing packages

Uninstall all packages

```
pip3 freeze | xargs pip3 uninstall -y
```
