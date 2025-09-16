# 📝 DAIICT B.Tech Student Data Analysis

## Introduction

This project provides a detailed analysis of survey data from B.Tech students at DAIICT. The main objective was to clean a raw dataset, perform an exploratory data analysis, and uncover insights that could be valuable for the institution. The analysis looks at student demographics, academic backgrounds, and how these factors relate to their performance and choices.

The project culminates in a set of findings and strategic recommendations covering the institute's marketing efforts and admissions policies.

***

## The Dataset 📊

The data comes from a survey of **202 B.Tech students** and originally contained **29 columns**. The key features used in this analysis include:

* **Demographics:** `Age`, `Sex`, `State`, `Family Size`, `Family Income`, `Joint Family?`
* **Academic Background:** `Rank JEE`, `12th grades`, `Dropped?`
* **University Metrics:** `SID` (Student ID), `Latest CGPA`
* **Student Feedback:** `Higher study?`, `TEACHING`, `INFRA`, `SPORTS`, `HOSTEL`
* **Lifestyle:** `CELL PHONE`, `STUDY`, `SLEEPING`

***

## Methodology ⚙️

The project was carried out in two main stages: first cleaning the data, and then exploring it through visualizations.

### 1. Data Cleaning and Preprocessing

The initial dataset had many inconsistencies, including missing values and varied data formats. Using libraries like Pandas and NumPy, a thorough cleaning process was undertaken:

* **Handling Missing or Irrelevant Data:** Columns like `COURSE` and `NAME` were dropped because they had too many missing values. Missing values in other critical columns were filled or handled on a case-by-case basis.
* **Standardizing Categorical Data:** Columns like `Sex`, `State`, and `Higher study?` had inconsistent entries (e.g., 'M', 'Male', 'MALE'). These were standardized into a uniform set of categories.
* **Cleaning Numerical Data:** Columns like `Family Income`, `Rank JEE`, and `12th grades` were particularly messy, containing a mix of text, numbers, and symbols. These were carefully parsed and converted into a consistent numerical format. For instance, `Family Income` was grouped into standardized income brackets for easier analysis.
* **Feature Engineering:** A new feature, 'Year of Admission', was created by extracting the year from the `SID` column. This allowed for trend analysis across different student batches.

### 2. Exploratory Data Analysis (EDA)

With a clean dataset, the Plotly library was used to generate visualizations to better understand the data. This included histograms to see the distribution of students across states and genders, box plots to examine academic trends over time, and scatter plots to investigate relationships between variables like college CGPA and 12th-grade marks.

***

## Key Findings and Recommendations 📈

### Key Findings

* **How Students Discover DAIICT:** The majority of students find out about DAIICT through their **schools**. The next most significant channels are **social media** and **family** referrals.
* **Demographic Snapshot:**
    * The student population is largely from **Gujarat (GJ)**.
    * The analysis revealed a gender ratio of about **four male students for every one female student**.
    * A large majority of students come from **nuclear families**.
* **Academic Admission Trends (2020-2024):**
    * There is a clear upward trend in the **median JEE rank** of admitted students over the last four years. In 2020, the median rank was around 25k, while by 2024, it had increased to approximately 40k-50k.
    * Recent years also show more outliers, with some students gaining admission with ranks as high as 200k.
    * This trend might be linked to the **GUJCET quota**, which allows Gujarat-based students to secure admission based on state-level exam scores and board results, placing less emphasis on JEE ranks.

### Recommendations

Based on these findings, the following strategic recommendations are suggested for the institute:

1.  **Optimize Marketing and Outreach:**
    * Strengthen partnerships with high schools, as this is the primary source of awareness for prospective students. This could involve hosting workshops and tech exhibitions on school campuses.
    * Increase investment in targeted social media campaigns on platforms like Instagram and LinkedIn, focusing on campus life and student achievements.

2.  **Refine Admissions Policy:**
    * To maintain academic standards, consider increasing the weightage of JEE scores for students applying through the Gujarat quota.
    * Implement a system to monitor the academic performance of students admitted through different channels and provide remedial support if needed.

By adjusting the admissions process and focusing on a competitive balance, DAIICT can continue to uphold its high educational standards while supporting regional students.

***

## Repository Contents 📂

* `Statistics_data_cleaning_and_EDA.ipynb`: The complete Jupyter Notebook with all Python code for data cleaning, preprocessing, and visualization.
* `DAIICT_Report.pdf`: A formal report summarizing the key findings and strategic recommendations from the analysis.
* `README.md`: This file.
* `all_btech_data.xlsx`: The raw, uncleaned dataset used for the analysis.
* `btechcleaned.csv`: The partially cleaned helper data used in the notebook.

***

## How to Run 🚀

To replicate this analysis, you can follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/DAIICT-Student-Analysis.git](https://github.com/your-username/DAIICT-Student-Analysis.git)
    cd DAIICT-Student-Analysis
    ```

2.  **Install the required libraries:**
    ```bash
    pip install pandas numpy plotly regex
    ```

3.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```

4.  Open and run the `Statistics_data_cleaning_and_EDA.ipynb` notebook to view the entire process.
