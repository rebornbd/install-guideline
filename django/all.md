### install django | step by step

#### step-01:
```python
# install python
# link: https://www.python.org/

# install pip || if needed
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py

# install virtualenv
pip install virtualenv
```

#### step-02:
```python
# create environment
C:\python\venv> virtualenv myvenv

# activate environment
C:\python\venv> myvenv\Scripts\activate
(myvenv) C:\python\venv>
```

#### step-03:
```python
# install django
(myvenv) C:\python\venv> pip install django
(myvenv) C:\python\venv> pip install django==2.2
```
