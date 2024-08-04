# math.biz.kdn.hu

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