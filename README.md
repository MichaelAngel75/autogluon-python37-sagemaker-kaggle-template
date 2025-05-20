# 🚀 Kaggle: Bike Sharing Demand (Python 3.7 Compatible)

This project is a starter template designed to work within a Python 3.7 environment. It is fully compatible with AWS SageMaker notebooks and AutoGluon v0.4.0 for machine learning workflows.

---

## 🧰 Key Features

- Python 3.7 support (legacy or restricted environments)
- Compatible with AutoGluon v0.4.0
- Custom kernel installation using `ipykernel`
- Dependency management via `pip` with version constraints
- Outputs can be exported to HTML or used for Kaggle submissions

---

## 📦 Installed Packages

- `autogluon.tabular==0.4.0`
- `mxnet==1.8.0.post0`
- `pandas==1.3.5`
- `matplotlib==3.5.2`
- `bokeh==2.4.3`
- `ConfigSpace==0.4.18`
- `ipykernel` (for custom Jupyter kernel)

---

## 📝 How to Use

### 1. Setup Environment


If running via Bash (e.g., in SageMaker Studio Labs or Jupyter Terminal), use:

```bash
conda create -n ag-gluon37 python=3.7 -y
conda activate ag-gluon37
pip install --upgrade pip setuptools==59.5.0 wheel==0.36.2
pip install pandas==1.3.5 matplotlib==3.5.2
pip install mxnet==1.8.0.post0 ConfigSpace==0.4.18
pip install bokeh==2.4.3
pip install autogluon.tabular==0.4.0 --no-cache-dir
pip install ipykernel
python -m ipykernel install --user --name ag-gluon37 --display-name "Python AFP (AutoGluon 3.7)"
```

### 2. Load Kernel in Jupyter Notebook

- Go to **Kernel > Change Kernel**
- Select **"Python AFP (AutoGluon 3.7)"**

---

## 🧪 Example Usage

```python
from autogluon.tabular import TabularPredictor

predictor = TabularPredictor(label='count').fit(train_data)
predictions = predictor.predict(test_data)
```

---

## 📤 Exporting Notebook as HTML

To save your notebook:
1. Go to `File > Download as > HTML (.html)`
2. Or run:  
   ```bash
   jupyter nbconvert --to html your_notebook_name.ipynb
   ```

---

## ✅ Recommendations

- Use `presets='best_quality'` for strong baseline results.
- Create validation plots and track improvement across:
  - Initial
  - Feature engineering
  - Hyperparameter tuning

---

## 📁 Folder Structure Suggestion

```
project-root/
├── project_notebook.ipynb
├── project_notebook.html
├── data/
│   └── train.csv, test.csv, submissions.csv
├── submissions  
│   └── submission-python-3-7.csv, submission_python-3-7-new_features.csv,  submission_python-3-7-hpo.csv (hyper-parameter optimized)
└── note.md
```

---

## 🧠 Author Notes

This project was developed for machine learning experimentation using AutoGluon in a constrained Python 3.7 environment. It emphasizes compatibility, clarity, and fast deployment in notebook-based workflows like SageMaker or Jupyter.

