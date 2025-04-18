# Beverage Container Recycling Analysis (British Columbia)

This repository contains a Python-based data analysis project focused on beverage container recycling in British Columbia, Canada. It combines and analyzes data from 29 regional districts alongside population estimates to explore trends in recycling over the period **2007–2017**.

## 📊 Project Objective

The primary goals of this project are:

- 🔹 To **combine** beverage recycling data (by region and year) with population estimates.
- 🔹 To **visualize** per-capita recycling activity by weight across regional districts.
- 🔹 To **produce a summary table** for the **entire province**, showing per-capita recycling trends over time.

## 📁 Dataset Overview

The analysis utilizes the following data files:

- **Population Estimates**:  
  `population_estimates.csv`  
  Contains columns: `regional_district`, `year`, `population`

- **Recycling Data**:  
  29 CSV files, one for each regional district (e.g. `Nanaimo.csv`)  
  Two formats:
  - *Long Format*: `year`, `measure`, `value`
  - *Wide Format*: `year`, `Units Collected`, `Weight Collected (Tonnes)`

## 🛠️ Tools & Libraries Used

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- OS module for file handling

## 📈 Visualizations & Outputs

### a. Per-Capita Recycling by Region (2007–2017)

A line plot showing **per-capita weight** (tonnes per person) of beverage containers recycled over time, broken down by regional district:

![Per Capita Recycling Plot](./assets/per_capita_plot.png)

### b. Provincial Summary Table

A table that summarizes **total weight** and **population** by year, with calculated **per-capita recycling** values for the entire province:

| Year | Total Weight (Tonnes) | Population | Per Capita Weight (Tonnes/Person) |
|------|------------------------|------------|-----------------------------------|
| 2007 | ...                    | ...        | ...                               |
| 2008 | ...                    | ...        | ...                               |
| ...  | ...                    | ...        | ...                               |

## 🧪 Methodology

1. **Load population data** and regional CSVs.
2. **Standardize** file names and validate coverage between regions.
3. **Pivot** long-format data into a usable wide format.
4. **Merge** population and recycling data per regional district.
5. **Filter** invalid rows (e.g., negative weights).
6. **Calculate per-capita metrics**.
7. **Visualize trends** and summarize provincial totals.

## 📂 File Structure

```
project6/
├── population_estimates.csv
├── [Regional District].csv  # 29 files
├── main_analysis.py         # Python code
├── README.md
└── assets/
    └── per_capita_plot.png  # Optional plot image
```

## 🚀 How to Run

Ensure all required CSV files are downloaded and located in the specified directory.

```bash
# Clone the repository
git clone https://github.com/your-username/project6-bc-recycling.git
cd project6-bc-recycling

# Run the analysis
python main_analysis.py
```

> Update the file paths in the script according to your local directory structure.

## 📌 Notes

- Some files may be in different formats; the script automatically detects and adjusts.
- Missing or invalid entries are skipped during merge.
- The analysis focuses only on the **years 2007 to 2017** as covered in the dataset.

## 📄 License

MIT License. See `LICENSE` for more info.

---

Made with 💚 for sustainable data.
