# mobile-net-mushroom-classification
Fine Tuning of MobileNetV2 to classify edibility of mushrooms from images

To run the notebook:

1. Install and configure pyenv (if you don't have it)
```bash
brew update
brew install pyenv
brew install brew install pyenv-virtualenv
```
2. Add pyenv to shell config
```bash
nano ~/.zshrc
```

then add to file

```bash
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"

eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

save and quit, source

```bash
source ~/.zshrc
```

3. Install Python 3.10
```bash
pyenv install 3.10.13 # tensorflow-metal works only until python 3.10
```
4. Create a virtual environment
```bash
pyenv virtualenv 3.10.13 tfmacos-310
pyenv activate tfmacos-310
```

5. Register the environment as Jupyter kerne;
```bash
python -m ipykernel install --user --name=tfmacos-310 --display-name "Python (tfmacos-310)"
```

6. Install requirements
```bash
pip install -r requirements.txt
```
7. restart your IDE
8. run the `.ipynb` notebook