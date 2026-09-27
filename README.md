# Python Job Market Analysis

This folder contains five Jupyter notebooks exploring job-posting data with Python. Together, they examine where data analyst jobs are posted, which skills are requested, how skill demand changes over time, and how skill demand relates to salary.

## Notebook Guide

| Notebook | Focus | Analysis and visualizations |
| --- | --- | --- |
| [1_](1_.ipynb) | US Data Analyst job market | Filters Data Analyst postings in the United States; ranks job locations and companies; visualizes the top locations and companies with bar charts; compares work-from-home, degree-mention, and health-insurance indicators with pie charts. |
| [2_](2_.ipynb) | Skills across data roles | Counts skills in US postings for Data Scientists, Data Engineers, and Data Analysts; calculates each skill's share of postings; compares each role's leading skills using horizontal bar charts, including percentage labels. |
| [3_](3_.ipynb) | Monthly skill trends | Explodes Data Analyst skill lists for US postings, aggregates skill counts by posting month, converts counts to percentages of monthly job postings, and plots monthly trends for the five leading skills. |
| [4_](4_.ipynb) | Data Engineer skills and pay | Measures skill frequency and median annual salary in Data Engineer postings; compares demand and salary in labeled scatter plots; consolidates the dataset's skill taxonomy into technology categories. |
| [5_](5_.ipynb) | Optimal skills for US Data Analysts | Uses US Data Analyst postings with salary information to calculate skill frequency, posting share, and median salary; plots skills appearing in more than 5% of this salary-filtered subset, with points grouped by technology category. |

## Visual Work

The notebooks contain the analysis and its chart outputs. Visualizations include:

- Bar charts of job counts by location, company, and skill.
- Pie charts comparing selected job attributes.
- Monthly line charts of skill prevalence.
- Scatter plots comparing skill demand with median annual salary.
- Technology-category groupings for skills in the salary analysis.

The charts are stored as notebook outputs, not as separate image files. Re-run the relevant notebook cells to regenerate them.

## Data and Tools

The notebooks load the `lukebarousse/data_jobs` dataset from Hugging Face using the `datasets` package. They use pandas and NumPy for data preparation, Matplotlib and Seaborn for charts, and `adjustText` to reduce overlapping plot labels. Python's standard-library `ast` module is used to parse skill fields.

Install the external packages in the Python environment selected by Jupyter:

```bash
python -m pip install datasets pandas numpy matplotlib seaborn adjustText
```

The dataset is fetched when the notebooks run, so initial loading requires an internet connection. Open a notebook in Jupyter and run its cells from top to bottom to reproduce the analysis.

## Notebook Status

Notebooks [4_](4_.ipynb) and [5_](5_.ipynb) contain successful execution counts. Notebooks [1_](1_.ipynb), [2_](2_.ipynb), and [3_](3_.ipynb) have saved outputs, but do not currently record successful execution counts; rerun them to verify the results in the current environment.

## Scope Notes

- Notebooks 1-3 explore job location, job attributes, skills, and monthly demand; notebooks 4-5 focus on salary comparisons.
- Notebook 5's skill percentages and salary comparisons are based on US Data Analyst postings that have a reported annual salary, not every posting in the dataset.
- These notebooks are exploratory analyses; they do not export a standalone report or dashboard.