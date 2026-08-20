# KLAB Python for AI - Assignment 1

This repository contains my Day 1 Python for AI warm-up assignment.

## 1. Clone the Repository

```bash
git clone https://github.com/Annemarie535257/K-LAB.git
cd K-LAB
```

## 2. Create and Activate the Virtual Environment

Create the virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

## 3. Install Dependencies

Install the required packages using:

```bash
pip install -r requirements.txt
```

## 4. Run the Smoke Test

After activating the virtual environment, start Jupyter Notebook:

```bash
jupyter notebook
```

Run the following cell in the assignment notebook:

```python
import numpy, pandas, sklearn, matplotlib
print("all good")
```

Expected output:

```text
all good
```

## 5. Open and Run the Assignment Notebook

From the repository root, start Jupyter Notebook:

```bash
jupyter notebook
```

Open the `Notebooks` folder and select:

```text
day01_assignment.ipynb
```

Then run all cells from top to bottom using:

```text
Kernel → Restart & Run All
```

If using VS Code, open the notebook and click **Run All** at the top.

The notebook should complete without errors.