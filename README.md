# math.biz.kdn.hu

Jupyter notebook project, replicating business mathematics charts.

- Used examples
  - MNB (Hungarian National Bank) educational publications 
  - Economics by Paul A. Samuelson, William D. Nordhaus

## Python setup

```bash
sudo apt install python3-pyenv

curl https://pyenv.run | bash

vim ~/.bashrc
### ~/.bashrc:
  export PYENV_ROOT="$HOME/.pyenv"
  [[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
  eval "$(pyenv init -)"
###

pyenv virtualenv math.biz
pyenv activate math.biz


pip install pip-tools

pip-compile ./requirements.in
pip-sync
```

## Git pre commit hook

```bash
#!/bin/sh
jupyter nbconvert --clear-output --inplace notebooks/*.ipynb
jupyter nbconvert --clear-output --inplace notebooks/*/*.ipynb

git add .
```

# Sources

## Economics 19th Edition
### by Paul A. Samuelson, William D. Nordhaus

- https://www.amazon.com/Economics-Paul-Samuelson/dp/0073511293
- https://mersz.hu/samuelson-nordhaus-kozgazdasagtan//

## MNB Oktatási füzet

https://www.mnb.hu/kiadvanyok/korabbi-kiadvanyok/oktatasi-fuzetek

https://www.mnb.hu/letoltes/mnb-oktatasi-fuzetek-2016-2szam-kotvenymatematika.pdf