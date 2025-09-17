## ML Practice

A curated set of Jupyter notebooks for practicing data science and machine learning concepts. This repo contains hands-on explorations, notes, and small examples using NumPy, pandas, Matplotlib, Seaborn, and FastAPI + SQLAlchemy.


[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](./LICENSE)

---

### Table of Contents
- [Contents](#contents)
- [Quick Start](#quick-start)
- [Running the FastAPI examples (optional)](#running-the-fastapi-examples-optional)
- [Repository Structure](#repository-structure)
- [Tips](#tips)
- [Troubleshooting](#troubleshooting)
- [Recommended VS Code Extensions](#recommended-vs-code-extensions)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

### Contents
- [`numpy.ipynb`](./numpy.ipynb): Core NumPy operations, array creation, indexing, broadcasting.
- [`pandas_prac.ipynb`](./pandas_prac.ipynb): Practical pandas exercises (Series, DataFrame ops, joins, groupby).
- [`pandas_test.ipynb`](./pandas_test.ipynb): Additional pandas tests and snippets.
- [`matplotlib.ipynb`](./matplotlib.ipynb): Plotting with Matplotlib (line, bar, scatter, styling).
- [`seaborn.ipynb`](./seaborn.ipynb): Statistical plotting with Seaborn (distributions, categorical, regression).
- [`FastAPI_SQLAlchemy_Roadmap.ipynb`](./FastAPI_SQLAlchemy_Roadmap.ipynb): Notes and examples to build REST APIs with FastAPI and SQLAlchemy.
- [`my_code_notes.ipynb`](./my_code_notes.ipynb) / [`notes_1.ipynb`](./notes_1.ipynb): Personal notes, tips, and reference snippets.

> All notebooks are self-contained and can be run independently.

---

### Quick Start

#### 1) Prerequisites
- Python 3.9+ recommended
- PowerShell (Windows) or a terminal

#### 2) Create and activate a virtual environment (PowerShell)
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If activation is blocked by script execution policy:
```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

#### 3) Install dependencies
If you already have a `requirements.txt`, use it. Otherwise, install a minimal set:
```powershell
pip install --upgrade pip
pip install jupyter numpy pandas matplotlib seaborn fastapi sqlalchemy uvicorn
```

#### 4) Launch Jupyter
```powershell
jupyter notebook | cat
```
Then open the desired notebook from the browser.

---

### Running the FastAPI examples (optional)
Some notes cover FastAPI + SQLAlchemy.

- Install (if not installed):
```powershell
pip install fastapi sqlalchemy uvicorn
```
- Minimal run pattern (example):
```powershell
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```
Adjust the import path to match your local example if you export code from the notebooks.

---

### Repository Structure
```
ml_practice/
├─ FastAPI_SQLAlchemy_Roadmap.ipynb
├─ matplotlib.ipynb
├─ my_code_notes.ipynb
├─ numpy.ipynb
├─ pandas_prac.ipynb
├─ pandas_test.ipynb
├─ seaborn.ipynb
├─ README.md
└─ LICENSE
```

---

### Tips
- Prefer running notebooks inside a virtual environment to keep dependencies isolated.
- Restart kernels regularly to ensure cells don’t rely on stale state.
- For large datasets, consider reading with `chunksize` in pandas and sampling for plots.
- In notebooks, set a consistent random seed when demonstrating stochastic methods.

---

### Troubleshooting
- Jupyter kernel not starting: ensure the correct interpreter is selected and the venv is active.
- Plots not showing in notebooks: add `%matplotlib inline` in a cell at the top.
- `ModuleNotFoundError`: verify the kernel uses the same environment where you installed packages.
- Activation policy on Windows: use `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`.
- Slow plots with large data: downsample or use `sns.relplot(..., height=...)` with fewer points.

---

### Recommended VS Code Extensions
- Python (Microsoft)
- Jupyter (Microsoft)
- Pylance (Microsoft)
- isort / Black (optional, for formatting)

---

### Roadmap
- [ ] Add scikit-learn notebook with basic models and evaluation
- [ ] Add EDA workflow notebook (missing values, outliers, feature types)
- [ ] Expand Seaborn notebook with facet grids and custom themes
- [ ] Export FastAPI examples from notebook to a small runnable app
- [ ] Create a `requirements.txt` with pinned versions

---

### Contributing
This is a personal practice space, but suggestions are welcome. Feel free to:
- Open an issue with ideas, corrections, or questions.
- Submit a small PR that improves clarity or fixes mistakes in notebooks.

Please keep examples simple and focused.

---

### License
This project is licensed under the terms of the `LICENSE` file included in the repository.
