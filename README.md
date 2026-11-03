# Second Highest Salary: Mini Analysis

Find the second-highest salary and compare approaches that scale.



An advanced data engineering and analysis project exploring hidden data traps (text formatting, missing values, and duplicate ties) when calculating the second-highest salary from messy datasets.



## Project Overview

Standard SQL and Pandas queries often assume clean data. This project replicates a real-world analytics workflow where raw data introduces hidden traps that break naive implementations:

**Data Type Trap:** Salary values formatted as strings with commas (`"198,000"`) causing alphabetical sorting errors instead of numerical ones.

* **Missing Data Trap:** Null or blank salary records requiring explicit handling.

* **Duplicate Ties:** Managing top-earning ties to correctly isolate the true \*distinct\* second-highest salary.



## Tech Stack

* **Language:** Python

* **Libraries:** Pandas, NumPy

* **Environment:** Jupyter Notebook



## Key Findings & Report to Compensation Team

* **Confirmed Value:** The second-highest distinct salary is **198,000**.

* **Data Repair:** Repaired formatting on error causing cells rather than dropping them, preventing faulty outputs.

* **Scalability:** Evaluated multiple computation approaches ($O(n)$ aggregate passes vs. $O(u \log u)$ sorting vs. $O(n \log n)$ window ranking) for future production runs.

---
**Note:** The raw dataset used for this analysis is proprietary and sourced from a third-party platform. To comply with terms of service, the raw data file is excluded from this repository. However, the complete data cleaning, validation, and ranking logic can be reviewed directly in the Jupyter Notebook



---

*Acknowledgements: Dataset structure and case study concept adapted from [StrataScratch Data Projects](https://platform.stratascratch.com/).*

