# deploy django on heroku steps:

#### step-01:

```
install git [if you don't have git]
```

```
create python env [if you don't have env]
activate env

create a django project
    django-admin startproject myproject

create a django app
    python manage.py myapp
```

django-app-configuration: [LINK](https://devcenter.heroku.com/articles/django-app-configuration)
```
pip install gunicorn
pip install django-heroku

import django_heroku              [add top of settings.py]
django_heroku.settings(locals())  [add bottom of settings.py]
```
settings.py
```python
import os
import django_heroku

BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))

................
................

STATIC_URL = '/static/'

django_heroku.settings(locals())
```

#### step-02:

add three files:
```
Procfile
runtime.txt
requirements.txt
```
Procfile
```
web: gunicorn myproject.wsgi
```
##### NB: myproject.wsgi [project-name.wsgi, where the wsgi is located: projectName/wsgi.py]

runtime.txt [python version]
```
python-3.7.9
```

requirements.txt [run the command]
```shell
pip freeze > requirements.txt
```

#### step-03:
django settings.py:
```
set: DEBUG = False
set: ALLOWED_HOSTS = [ 'heroku_appname.herokuapp.com', '127.0.0.1', 'localhost']
set: MIDDLEWARE = [ ............................................
                    'whitenoise.middleware.WhiteNoiseMiddleware',
                    .............................................
                    ..............................................
                  ]
set: STATIC_ROOT = os.path.join(BASE_DIR, 'static')
set: STATICFILES_DIRS = [ os.path.join(BASE_DIR, 'static'), ]
```

final settings.py:
```python
import os
import django_heroku

BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))

DEBUG = False
ALLOWED_HOSTS = [ 'heroku_appname.herokuapp.com', '127.0.0.1', 'localhost']
................
................

MIDDLEWARE =  [ ............................................
                'whitenoise.middleware.WhiteNoiseMiddleware',
                .............................................
                ..............................................
]

STATIC_URL = '/static/'

STATIC_ROOT = os.path.join(BASE_DIR, 'static')
STATICFILES_DIRS = [ os.path.join(BASE_DIR, 'static'), ]

django_heroku.settings(locals())
```


