# ml-competition-template-titanic

- [Kaggle Titanic](https://www.kaggle.com/c/titanic) example of my own, folked from [upura's repo](https://github.com/upura/ml-competition-template-titanic)
- You can get the score = 0.76555 at the version of 2018-12-28.
- Japanese article can be seen [here](https://upura.hatenablog.com/entry/2018/12/28/225234).

## Note

Use [kaggle/python](https://github.com/Kaggle/docker-python) container.

## Structures

```
.
├── configs
│   └── default.json
├── data
│   ├── input
│   │   ├── sample_submission.csv
│   │   ├── train.csv
│   │   └── test.csv
│   └── output
├── docker-run.sh
├── features
│   ├── __init__.py
│   ├── base.py
│   └── create.py
├── logs
│   └── logger.py
├── models
│   └── lgbm.py
├── notebooks
│   └── eda.ipynb
├── scripts
│   └── convert_to_feather.py
├── utils
│   └── __init__.py
├── .gitignore
├── .pylintrc
├── LICENSE
├── README.md
├── run.py
└── tox.ini
```
## Commands

### EDA by Jupyter Notebook

```
docker-run.sh jp
```

### Change data to feather format

```
docker-run.sh py scripts/convert_to_feather.py
```

### Create features

```
docker-run py features/create.py
```

### Run LightGBM

```
docker-run.sh py run.py
```

### flake8

@todo: modify

```
flake8 .
```
