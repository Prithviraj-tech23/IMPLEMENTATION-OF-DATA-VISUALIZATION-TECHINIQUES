
# E-commerce Transactions Visualization (R)

**Name:** P S S PRITHIVI RAJ  
**Roll No:** 23BAD088  

This project uses **R** to perform basic exploratory data analysis (EDA) on an e-commerce transactions dataset and generates three visualizations:

1. **Histogram of Transaction Amounts**
2. **Boxplot for Outlier Detection**
3. **Monthly Sales Heatmap**

---

##  Requirements
- R (4.0+ recommended)
- Packages:
  - `ggplot2`
  - `dplyr`
  - `lubridate`

Install the packages (run once):

install.packages(c("ggplot2", "dplyr", "lubridate"))


Load libraries:


library(ggplot2)
library(dplyr)
library(lubridate)


## Dataset

Place the dataset file in the same folder as the script:

`ecommerce_transactions.csv`

The script reads:


ecommerce_data <- read.csv("ecommerce_transactions.csv")

---

## Expected Columns in CSV

Your CSV must include at least these columns:

* `Transaction_Amount` (numeric)
* `Transaction_Date` (date string, preferably `YYYY-MM-DD`)

Example:

| Transaction_Amount | Transaction_Date |
| ------------------ | ---------------- |
| 499.50             | 2024-01-15       |
| 1299.00            | 2024-02-03       |

---

## How to Run

1. Download/clone this repository.
2. Open RStudio.
3. Open the script file (example: `EDA2.R`).
4. Run the script, or use:

```IN r
source("ecommerce_analysis.R")
```

(Use your actual script filename if it’s different.)

---

##  What the Script Does

### 1) Data Cleaning

* Removes missing values:

```IN r
ecommerce_data <- na.omit(ecommerce_data)
```

### 2) Histogram

* Shows distribution of transaction amounts using a histogram.

### 3) Boxplot

* Detects outliers in transaction amounts using a boxplot.

### 4) Monthly Sales Heatmap

* Converts `Transaction_Date` into monthly format using:

```IN r
floor_date(as.Date(ecommerce_data$Transaction_Date), "month")
```

* Groups totals by month and visualizes total sales intensity with a heatmap.

---

##  Notes

* Ensure `Transaction_Date` values are valid dates.
* Plots will appear in the **Plots** panel in RStudio.
* To save plots, you can use `ggsave()` (optional).

---

## 👤 Author

**P S S PRITHIVI RAJ**
**Roll No:** 23BAD088

```
```
