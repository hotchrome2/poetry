# poetry on Windows11
## decibel

py -0

poetry new decibel

cd decibel

poetry config virtualenvs.in-project true --local

py -3.11 -c "import sys; print(sys.executable)"

poetry env use C:\Users\admini7\AppData\Local\Programs\Python\Python311\python.exe

poetry run python --version

- bad
  -  poetry add pandas seaborn jupyterlab matplotlib lckr_jupyterlab_variableinspector jupyterlab_code_formatter
  - poetry add --group dev pytest pytest-mock mypy black isort icecream
  - poetry add lightgbm

poetry show

## artificial

poetry new artificial

cd .\artificial\

poetry config virtualenvs.in-project true --local

py -3.13 -c "import sys; print(sys.executable)"

poetry env use C:\Users\admini7\AppData\Local\Programs\Python\Python313\python.exe

poetry run python --version

- bad
  - poetry add pandas seaborn jupyterlab matplotlib lckr_jupyterlab_variableinspector jupyterlab_code_formatter scikit-learn
  - poetry add --group dev pytest pytest-mock mypy black isort icecream
  - poetry add lightgbm
  - poetry add tqdm

poetry show

---
## Good add

poetry add numpy pandas seaborn tqdm jupyterlab matplotlib scikit-learn lightgbm

poetry add --group dev pytest pytest-mock mypy black isort icecream lckr_jupyterlab_variableinspector jupyterlab_code_formatter

