# Django first

## Overview
- Create site and apps on Django at first time

## History

- created date : 2018/06/02

## Environment

- below:

``` powershell
PS G:\> python --version
Python 3.6.5
PS G:\> virtualenv --version
16.0.0

```
- Using virtualenvwrapper

## Installation
- virtual environment

``` powershell
PS G:\> dir Env: | out-string -stream | select-string "WORKON"

WORKON_HOME                    G:\env\py

PS G:\> mkvirtualenv djfirst
PS G:\workplace\py\djfirst> cd $Env:WORKON_HOME
PS G:\env\py> .\djfirst\Scripts\activate

```

- python package installation
```
(djfirst) PS G:\env\py> pip install -r requirements.txt
```
## Execution

```
(djfirst) PS G:\> dir Env: | out-string -stream | select-string "WORKON|PROJECT"

PROJECT_HOME                   G:\workplace\py
WORKON_HOME                    G:\env\py


(djfirst) PS G:\> cd $Env:PROJECT_HOME
(djfirst) PS G:\workplace\py> cd .\djfirst\
(djfirst) PS G:\workplace\py\djfirst> ls


    Directory: G:\workplace\py\djfirst


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----         6/2/2018   7:55 AM                djfirst
d-----         6/1/2018  11:01 PM                hello
-a----         6/2/2018   6:39 AM             35 .gitignore
-a----         6/1/2018   6:59 AM              0 db.sqlite3
-a----         6/1/2018   6:56 AM            554 manage.py
-a----         6/2/2018   6:43 AM            144 README.md
-a----         6/2/2018   8:18 AM             60 requirements.txt


(djfirst) PS G:\workplace\py\djfirst> python manage.py runserver
Performing system checks...

System check identified no issues (0 silenced).

You have 14 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
June 02, 2018 - 08:22:02
Django version 2.0.5, using settings 'djfirst.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CTRL-BREAK.
```

- access http://127.0.0.1:8000/

// --- end of file
