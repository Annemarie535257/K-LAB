# Assignment 2: Data Wrangling and Exploratory Analysis

This assignment applies **NumPy, Pandas, and Matplotlib** to a real-world housing dataset.

## Dataset

**Dataset name:** House Price Prediction
**Source:** Kaggle
**Source URL:** https://www.kaggle.com/datasets/shree1992/housedata
**License:** Unknown (as listed on Kaggle)

I chose this dataset because it contains more than 200 rows and includes both numeric and categorical variables.

The dataset contains housing information such as house price, bedrooms, bathrooms, living area, lot size, property condition, waterfront status, street, city, and construction year.

It is suitable for practicing data cleaning, Pandas transformations, NumPy computations, and exploratory data analysis.

## Analysis Question

**How do living space and location relate to house prices?**

## Repository Structure

```text
K-LAB/
├── Notebooks/
│   └── assignment2_house_analysis.ipynb
├── data/
│   ├── raw/
│   │   └── data.csv
│   └── processed/
│       └── house_prices_cleaned_featured.csv
├── reports/
│   ├── a2_chart1.png
│   ├── a2_chart2.png
│   └── Assignment2_report.md
└── README.md
```

## Running the Notebook

Activate the virtual environment.

On Windows PowerShell:

```bash
.venv\Scripts\Activate.ps1
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Notebooks/assignment2_house_analysis.ipynb
```

Then select:

**Kernel → Restart & Run All**

## Output Files

The cleaned and feature-engineered dataset is saved to:

```text
data/processed/house_prices_cleaned_featured.csv
```

The visualizations are saved to:

```text
reports/a2_chart1.png
reports/a2_chart2.png
```

The final analysis report and reflection are saved to:

```text
reports/Assignment2_report.md
```

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook