# Cooking and Ordering Trends: A Comprehensive User Behavior Analysis 

The objective of this analysis is to explore datasets that provide insights into user behavior, cooking preferences, and order trends. By examining these patterns, the aim is to uncover actionable insights that can inform business strategies and improve user engagement.


## Overview

**Project Name**: Cooking and Ordering Trends: A Comprehensive User Behavior Analysis  
**Tools and Technologies:**

**Programming Languages:**

**Python-** For data cleaning, merging, analysis, and visualization.

- **Data Analysis Libraries:**

**Pandas-** For data manipulation, merging datasets, and generating insights.

**NumPy-** For numerical computations.

- **Data Visualization Libraries:**

  **Matplotlib-** For creating line plots, bar charts, and pie charts to visualize trends and distributions.

  **Seaborn-** For advanced data visualizations, including heatmaps and categorical plots.

- **IDE/Platform:**

  **Jupyter Notebook-** For interactive programming and visualization during the analysis.

- **Version Control:**

**Git and GitHub-** For managing project versions and uploading the Jupyter Notebook for collaboration and sharing.

- **Data Formats:**

**CSV Files-** As the primary format for storing user details, cooking sessions, and order details.

- **Statistical Techniques:**

**Correlation Analysis-** To find relationships between cooking sessions and orders.

**Descriptive Statistics-** To summarize numerical data, like average session duration and order frequency.

**Data Sources:**
The data analyzed in this report was obtained from the culinary app platform during the period of January 2023 to December 2023. 

**User Data:** Demographic details such as age, gender, and location.
**Data from Cooking Sessions:** Records of cooking sessions that include timestamps, the dishes prepared, and the length of the session.
****Order Data: Details on placed orders, such as dish names, dates, and amounts.

# Methodology: Data Cleaning, Merging, and Analysis Techniques
### Data Cleaning:

**1. Inspecting the Structure of DataFrames:**

Each DataFrame's structure (user_details, cooking_sessions, and order_details) was examined using .info() to comprehend the types of data, column names, and memory utilization.
This gave a summary of the datasets and made it easier to see duplicate entries, missing values, and possible data type inconsistencies in the columns.

**2. Checking for Missing Values:**

Identified missing values in each DataFrame using .isnull().sum().
Dropna() was used to eliminate missing data in order to preserve the analysis's integrity. This made sure the findings weren't skewed by any missing records.

**3. Identifying and Removing Duplicate Entries:**

Checked for duplicate rows using .duplicated().sum().
Duplicates were removed using .drop_duplicates() to avoid overrepresentation of any data point.

**4. Standardizing Column Names:**

standardized column names by using.str.lower() and.str.replace() to change spaces to underscores and convert them to lowercase.
This guaranteed consistency between datasets, which facilitated programmatic data manipulation and merging.

**5. Generating Descriptive Statistics:**

describe() was used to compute summary statistics for the numerical columns in each of the three datasets.
This made it possible to spot possible outliers, inaccurate data points, and broad patterns in the numerical data, enabling any necessary additional repairs.

**6. Maintaining Data Consistency:**

Ensured all necessary steps were taken to preserve data consistency, enabling seamless merging and analysis across multiple datasets.
Purpose of Data Cleaning:
The goal of data cleaning was to improve accuracy, reduce variability in the datasets, and guarantee the validity of the conclusions derived from the research. The groundwork for combining datasets and carrying out insightful analysis was laid by standardizing the data and eliminating errors.

This methodical approach to data cleaning was crucial in getting the data ready for additional investigation and the creation of new insights.

### Data Merging:
To conduct the analysis, multiple datasets were merged to create a unified view of user behavior, cooking preferences, and order trends.

**1. Initial Merge:**

Using the user_id column as the primary key, the user_details and cooking_sessions datasets were combined.
This made it possible for us to relate consumers to their culinary activities by combining data from their cooking sessions with user demographics.

**2. Second Merge:**

The resulting DataFrame from the first merge was further merged with the order_details dataset using the user_id column as the key.
By integrating order data, this stage made it possible to analyze how cooking sessions affected user behavior and order trends.

**3. Validation:**

To make sure the merging procedure was effective and the final dataset included required details from all three sources, the structure of the merged data was examined using.head() after each merge.

**4. Purpose of Merging:**

The goal of the merger was to allow for a thorough examination of the connections among user demographics, cooking sessions, and order trends. When these datasets are combined:

We could examine the relationship between ordering patterns and cooking behavior.
It was possible to spot trends among various user demographics.
It might yield information about user preferences and involvement.

# Analysis Techniques:
The analysis employed a combination of statistical and visualization techniques to extract meaningful insights from the merged dataset. These methods allowed us to uncover patterns, behaviors, and trends that inform actionable business decisions.These methods allowed us to uncover patterns, behaviors, and trends that inform actionable business decisions. The following techniques were used:

- #### **Trend Analysis:**
    Finding trends in user activity and ordering behavior over time is the goal.

  **Method:** Trends in orders over time were shown using line plots, which shed light on seasonal patterns and periods of high activity.

- #### **Descriptive Statistics:**
    **Objective:**
    Compile data on user behavior, such as the length of a cooking session, the frequency of orders, and the popularity of a meal.

    **Method:**
    To comprehend typical user behavior, averages and medians for metrics like cooking-to-order ratios were computed.
    Using the.value_counts() function on the dish_name column, the most popular dishes during cooking sessions were determined.

- #### **Ratio Analysis (Cooking-to-Orders):**
   **Objective:** Understand user engagement by analyzing the ratio of completed orders to cooking sessions.

   **Method:**
   Used a grouped ratio calculation, dividing the number of completed orders by the number of cooking sessions for each user:
   The results provided an understanding of how many cooking sessions translated into actual orders.

- #### **Location-Based Analysis:**
   **Objective:** Assess cooking and ordering behaviors across different locations to identify geographic trends.

   **Method:** Data was grouped by location, and for each location, the ratio of completed orders to total sessions was determined:
   Areas with greater rates of order completion and user involvement were highlighted by this analysis.

- #### **Correlation Analysis (Heatmaps):**
   **Objective:** Identify relationships between demographic factors (e.g., location, age) and user behavior.

  **Method:** Divided the total number of orders fulfilled by the total number of cooking sessions for each user using a grouped ratio 

- #### **Clustering:**
   **Objective:** Segment users based on cooking-to-order ratios and behavioral patterns.

  **Method:** To help identify different user personas (e.g., frequent chefs, casual users, or high-order users), clustering was used 
   to group individuals with comparable ratios.

The importance of techniques
Using these methods, the analysis yielded useful information about:

User preferences and popular foods.
patterns of behavior in various locales and demographics.
important elements influencing order completion rates and user engagement.

# Key Insights
#### 1. Popular Dishes
The analysis of popular dishes revealed significant preferences among users:
**2. Most Popular Dishes:**
Spaghetti Bolognese topped the list
#### 3. Visual Insights:
A pie chart was created to depict the distribution of users' favorite meals
Insights from this visualization supported targeted meal promotions.
#### 4. Order Trends:
Users who spent less than 20 minutes in cooking sessions were 40% more likely to place frequent orders, suggesting a preference for quick meals.
A strong correlation (r = 0.4743) was identified between session ratings and total orders
#### 5. Visualization of Orders Over Time:
A time-series plot highlighted seasonal and weekly ordering patterns
Demographics Influencing Behavior
#### 6. User behavior varied across age groups, genders, and locations:
**Age:**
- Younger users (18-25 years) showed a preference for fast, easy-to-cook meals and placed 20% more orders than other age groups.
- Older users (40+ years) spent more time cooking (average session duration: 45 minutes) and placed fewer orders.
A stacked bar chart visualized total orders by location and favorite meal
#### Location Distribution:

A pie chart illustrated the geographic distribution of users

**Summary of Insights**

The most popular food is spaghetti, though regional preferences differ.
Weekends and evenings see an increase in cooking sessions, which affects order trends.
Age and geography are two demographic factors that have a big impact on ordering and cooking habits.

# Business Recommendations
#### 1. Promote Popular Dishes:
Highlight the top three dishes (Spaghetti ,Grilled Chicken, caesar salad) in targeted ads.
Offer combo deals like "Spaghetti with Garlic Bread and Drink at 15% Off" for users 
#### 2. Reward Cooking Enthusiasts:
Introduce a loyalty program that rewards users after completing a set number of cooking sessions:

**Example:** "Cook 10 Meals and Get Your First 5 Orders at 10% Off."
#### 3. Exclusive Content and Features:
Offer high-frequency cooks access to premium content like:
- Exclusive recipes.
- Early access to new features such as "Personalized Meal Planner" or "Interactive Cooking Tutorials."
#### 4. Age-Based Campaigns:
Younger Users (18-25 years): Focus on fast, trendy meals and offer social sharing options:

**Example:** "Snap Your Dish and Get 5% Off Your Next Order!"























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
