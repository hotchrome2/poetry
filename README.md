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

### LightGBM
```python
params = {
    "objective": "mae",  # 目的関数
    "learning_rate": 0.01,  # 学習率
    "reg_lambda": 1.0,  # L2正則化項
    "reg_alpha": 0.1,  # L1正則化項
    "max_depth": 10,  # 決定木の深さ
    "n_estimators": 2500,  # 決定木の数
    "colsample_bytree": 0.5,  # 各木を作成するときに使用可能な特徴量の割合
    "min_child_samples": 10,  # 末端ノードに含まれる最小のデータ数
    "subsample": 0.9,  # 各ツリーで選択されるサンプリングの割合
    "subsample_freq": 3,  # サンプリングの頻度
    "importance_type": "gain",  # 重要度の種類を指定 split:特徴がモデルで何回使われたか, gain:徴を利用した分割の総獲得数
    "random_state": RANDOM_STATE,  # 乱数シード
    "n_jobs": -1,  # 並列処理
    "device": "cpu",  # デバイス設定、GPU環境なら "gpu"を指定
    "max_bin": 100,  # 一つの分岐に入るデータ数の最大値
}
```
