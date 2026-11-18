# 🎓 Course Data Cleaning & Exploratory Data Analysis

A hands-on data analysis project that takes a raw, messy, header-less CSV of training institutes and courses across India, cleans it with Python and Pandas, and explores it through univariate, bivariate and grouped analysis with clear visualisations.

# 📌 Overview

The dataset (course.csv) lists institutes offering courses such as AI, ML, Data Science, AWS and Web Services in different Indian cities. The raw file had no header, spelling mistakes, wrong state codes and inconsistent institute names, so cleaning was a big part of the work.

The goal was to turn it into a clean dataset and answer practical questions such as:

- Which cities and states have the most institutes?
- Which courses are offered most often, and how long do they run?
- How do Data/AI courses compare with Cloud/Infrastructure courses?
- What share of courses are short-term versus long-term?

# 🧹 Data Cleaning Steps

| Issue found | Fix applied |
|-------------|-------------|
| No header row | Loaded with `header=None` and assigned column names |
| Spelling errors | `Channai` → `Chennai`, `Could` → `Cloud` |
| Inconsistent state codes | `Gj` → `GJ`, `BH` → `BR`, swapped mislabelled `KT`/`TN` codes (Chennai → `TN`, Bengaluru → `KT`) |
| Uneven spacing in institute names | Removed extra whitespace with `str.strip()` and `str.replace()` |
| Mixed institute suffixes (`.Pvt`, `.Pvt.LTD`, `.Ltd`, none) | Created `Institute_type` column: **Pvt Ltd / Ltd / Unspecified** |
| Duration stored as text | Extracted numbers into an integer column `Duration_Months` |
| Missing values / duplicates | Checked: none found |

New columns created: Institute_type, Duration_Months, Duration_Group (Short-term / Long-term), Category (Data/AI vs Cloud/Infrastructure)

# 🔍 Analysis Performed

- Univariate analysis
- Bivariate and multivariate analysis
- Grouping and insights

# 🛠️ Tech Stack
- Python (Pandas, NumPy)
- Matplotlib and Seaborn for visualisation
- Jupyter Notebook

# 👤 Author

Anush Surve 📧 anush.surve29@gmail.com 

⭐ If you found this project useful, consider giving it a star!
