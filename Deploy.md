## Deploying This Project

[Clich Here to See Live Demo](https://peppa.pythonanywhere.com/)

-> Make Sure you have Git Installed
Git Download
https://git-scm.com/download/win

-> Create a GitHub Account at
https://github.com/

-> Get Your Project files or grap mine here
https://github.com/Academy-Omen/django-portfolio

-> Create repository and Push the code to GitHub

-> Test django webapp and create django requirements files
``` bash
python manage.py runserver
python -m pip freeze > requirements.txt
```

-> Update Repository

-> Create Pythonanywhere account
https://www.pythonanywhere.com/registration/register/beginner/

-> Clone repository
``` bash
git clone https://github.com/itzomen/porto.git
```

-> Create a Virtual environment using
``` bash
mkvirtualenv --python=/usr/bin/python3.8 venv
```

-> Install all requirements using
``` bash
pip install -r requirements.txt
```
-> Setting up your Web app and WSGI file

```
Source code: /home/peppa/porto

Working directory: /home/peppa/

Virtual Environtment Path: /home/peppa/.virtualenvs/env

# Paths
/static/	/home/peppa/porto/static_root/

/media/	/home/peppa/porto/media_root/

```
-> WSGI
```
import os
import sys


path = os.path.expanduser('~/porto')

if path not in sys.path:
    sys.path.insert(0, path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'portfolio.settings'

from django.core.wsgi import get_wsgi_application

from django.contrib.staticfiles.handlers import StaticFilesHandler
application = StaticFilesHandler(get_wsgi_application())

```