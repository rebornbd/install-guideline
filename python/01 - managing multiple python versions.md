### Managing Multiple Python Versions With pyenv
------------------------------------------------

#### prerequisites(Ubuntu/Debian) [other os](https://github.com/pyenv/pyenv/wiki/Common-build-problems)
```shell
sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

#### installation pyenv [link](https://github.com/pyenv/pyenv-installer)
```shell
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash

nano ~/.bashrc

# add the below script under the files:
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

#### check | set | install | uninstall different python version
```python
# check
pyenv versions
pyenv install -list

# install
pyenv install 3.6.9
pyenv install 3.7.9
pyenv install 3.8.6

pyenv versions
python --version

# set
pyenv global 3.8.6

pyenv versions
python --version

# uninstall
pyenv uninstall 3.7.9
```

