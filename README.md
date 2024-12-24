# Cooking and Ordering Trends: A Comprehensive User Behavior Analysis 

The objective of this analysis is to explore datasets that provide insights into user behavior, cooking preferences, and order trends. By examining these patterns, the aim is to uncover actionable insights that can inform business strategies and improve user engagement.


## Overview

**Project Name**: Cooking and Ordering Trends: A Comprehensive User Behavior Analysis  
**Tools and Technologies**: Python, 
**Dataset**: [Indian Food 101](https://www.kaggle.com/datasets/nehaprabhavalkar/indian-food-101)  
**Project Duration**: December 16, 2024 - January 16, 2025 (excluding weekends, xmas + new year-end vacations)

## Objectives

- Analyze and organize cooking recipes
- Provide easy-to-follow instructions, ingredients, and cooking times
- Use Unsupervised Machine Learning techniques (e.g., Clustering)
- Develop interactive visualizations using Looker Studio

## Highlights

- **Data Collection and Cleaning**: Efficiently collected and cleaned the dataset to ensure accuracy.
- **Feature Engineering**: Extracted relevant features from the dataset for better analysis.
- **Machine Learning Models**: Implemented clustering algorithms to categorize recipes.
- **Interactive Dashboards**: Created user-friendly dashboards using Looker Studio for easy data visualization.

## Challenges

- Handling missing values and inconsistencies in the dataset.
- Ensuring the machine learning models accurately categorize recipes.
- Developing interactive and intuitive visualizations.

## Folder Structure

```plaintext
Cook-Me-Up/
│
├── data/
│   ├── raw/
│   │   └── indian_food.csv        # Original CSV file from Kaggle API Call
│   ├── processed/
│   │   └── cleaned_data.csv       # CSV file as a Result of Data Cleaning
│   └── BigQuery/
│       └── bigquery_output.csv    # CSV file as a Result of BigQuery SQL
│
├── notebooks/
│   ├── data_cleaning.py           # Documents the data cleaning process
│   ├── data_exploration.py        # Level 1 dataset EDA Python libraries Pandas, Numpy, Matplotlib, Seaborn
│   └── data_visualization.py      # Level 2 dataset EDA Seaborn, machine learning (Clustering etc.), input to Looker Studio
│
├── scripts/ 
│   ├── bigquery_eda.sql           # SQL script for initial exploratory data analysis using BigQuery
│   ├── bigquery_analysis.sql      # SQL script for more in-depth analysis, meaningful insights using BigQuery
│   └── visualization.sql          # SQL script for generating visualizations and input to Looker Studio
│
├── reports/
│   ├── EDA_report.md              # Markdown file documenting the exploratory data analysis
│   ├── results.md                 # Markdown file documenting the results of the analysis
│   └── final_presentation         # Folder containing the final presentation materials
│
├── streamlit/                     # Streamlit app files (through a side branch: streamlit_deployment)
│   ├── streamlit_app.py           # application script
│   └── indian_food.csv            # raw CSV file for Streamlit app
│
├── README.md
├── INSTRUCTIONS.md
├── LICENSE



```
### Prerequisites

- Python 3.x
- BigQuery account
- Looker Studio account

### License
This project is licensed under the MIT License. See the LICENSE file for details.

### Acknowledgments
- [WBS Coding School](https://github.com/WBSCodingSchool) for the support and guidance.
- Kaggle for providing the dataset.
- All contributors to this project.  
