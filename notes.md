## PART 1: SETUP AND INTRODUCTION

1- Install Vscode and python for Windows
https://www.python.org/downloads/windows/
https://code.visualstudio.com/download#


2- Overview of Django
Models-Viewa-Templates


3- Test python
`py -3 --version`

4- Create Virtual Environment where you install python packages to isolate from
other packages in your system
`py -3 -m venv env`

5- Activate Environment

Windows disable running such scripts, fix with
POWERSHELL as admin
Set-ExecutionPolicy RemoteSigned

`.\env\Scripts\activate`

6- Install Django
`python -m pip install django`
Test Django
`python -m django --version`

7- Start a new project in the directory
`django-admin startproject portfolio`

8- Check project
`python manage.py runserver`

9- Create an app
`python manage.py startapp john`

10- Add app to settings

11- Install Pillow which is a python Imaging Library
`python -m pip install Pillow `


---------------------------------------------------------------------
PART 2: MODELS AND ADMIN INTERFACE

https://docs.djangoproject.com/en/3.1/topics/db/models/
https://docs.djangoproject.com/en/3.1/ref/contrib/admin/


12- Create Models, and apply migrations
python manage.py makemigrations
python manage.py migrate

13- Create superuser
`python manage.py createsuperuser`

14- Add string methods
```python
def __str__(self):
        return str(self.id)
```

15- Configure static files path and urls
```python
STATIC_URL = '/static/'
MEDIA_URL = '/media/'

MEDIA_ROOT = os.path.join(BASE_DIR, 'media_root/')
STATIC_ROOT = os.path.join(BASE_DIR, 'static_root/')

STATICFILES_DIRS = [
    BASE_DIR / "static",
]
```

16- Tell Django where to find the static files while on the browser

```python
if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL,
                          document_root=settings.MEDIA_ROOT)
```


---------------------------------------------------------------------

PART 3: VIEWS AND TEMPLATES


17- Write basic view, add index.html in app template folder and configure 
app url

```python
def index(request):
    return render(request, 'index.html')
```
18- Add assets folder to static_root folder
- Frontend
https://github.com/bedimcode/responsive-portfolio-website-JhonDoe

19- Load static files in html file

20- Write Views

21- Add Data in Admin interface

22- Load content from views to Templates
```html
{% static 'assets/css/styles.css' %}

{{ model.field }}
```

---------------------------------------------------------------------
Check [DEPLOYMENT](Deploy.md)

