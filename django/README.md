# Install Django - (windows)


sort intro:
=============
01) pip install virtualenv
02) virtualenv myvenv
03) myvenv\Scripts\activate
04) pip install django
05) django-admin startproject myapp
06) cd myapp
07) python manage.py runserver


1'st step: (install python)
==========
			01) install manually specific python version globally

2'nd step: (create virtual environment)
==========
			op-01) python -m venv myvenv
			
			op-02)
					pip install virtualenv  ||  (globally-install-virtualenv)
					virtualenv myvenv
					
3'nd step: (activate virtual environment)
==========
			01) myvenv\Scripts\activate  ||  (E:\Python\myvenv\Scripts\activate)
			
			
4'th step: (install django)
==========
			01) pip install django  ||  (pip install django==2.0 | specific-version)
			
5'th step: (create project)
==========
			01) django-admin startproject myapp
			
6'th step: (run server)
==========
			01) cd myapp  ||  (go-to-project-folder)
			
			op-01) python manage.py runserver       ||  (default-port | 8000)
			op-02) python manage.py runserver 8200  ||  (mension-port)
			
