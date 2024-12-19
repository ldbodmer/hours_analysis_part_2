# RAS Data Analysis – Part 2

This repository contains a Jupyter Notebook focused on an secondary analysis of CRM data to explore trends in categorical data. 

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Key Features of the Analysis](#key-features-of-the-analysis)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [Next Steps](#next-steps)

---

## Project Overview

This is part two of a larger project. The overall project goal is to create a "scorecard" methodology for weighing searches by category, by liklihood of leading to contract, and by difficulty.
This second part focuses on identifying high-value cases based on type of case and subject area categorical variables.

The analysis separates the dataset into three categories based on number of total searches in each data grouping and the similarities of the groupings. 


---

## Dataset Description

The dataset includes:
- Searches created after January 1, 2020 up to October 2024 with complete hours data.
- Total Searches, contracts and billing information
- Division
- Source
- NOS
- Search Stage
- Type of Case
- Subject
- Hours Reported
- Dates related to search creation, contracts, billing, and completion.

---

## Key Features of the Analysis

**Data Preparation**:
- investigate IP separately across subject areas
- group antitrust, false claims act and criminal 
- group class action, tort, contract and unfiled.
- unicorn outlier is removed to not skew results

**Data Analysis**:
- correlations between total searches and billed hours
- correlations between total searches and billing contracts
- evaluate skewness of data for each group and transform if necessary
- compare total hours reported to total searches in each category

**Visualization**: 
- Create plots that give clear picture of trends 

---

## Dependencies
The analysis uses the following Python libraries:
- `pandas` - For data manipulation and analysis.
- `seaborn` - For advanced data visualization.
- `matplotlib` - For creating static plots.
- `numpy` - For numerical operations.

---

## Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/hours_analysis_part_2.git
   
2. Install required libraries:
   ```bash
   pip install pandas seaborn matplotlib numpy
3. Place the CSV file containing the dataset:
   (all_searches_created_after_january_2020.csv) in the repository directory.
5. Run the jupyter notebook:
   ```bash
   jupyter notebook hours_analysis_part_2.ipynb

---

## Visualizations
The notebook provides several visualizations to explore the following questions:

- Scatterplot with trend line: Is there a clear correlation between hours reported and searches created for both divisions? For total searches to contracts billed?
- Histogram: What is the skewness of the average billed hours data? Does it improve with transformation?
- Barplot: For each data set, what is the standard deviation above or below the average hours billed in that set?

---

## Conclusions
-  There is a clear trend and correlation between both searches created and hours billed and searches created and contracts billed. 
-  There were some surprises for categories that were underperforming in comparison to others. This relationship was difficult to see without normalizing the data. 
-  Confirmed  high performing categories.

---

## Next Steps
- what is the overall variability in the data?
- are there significant variations within each category?
- what is statistically significant number of searches in a category?
- how do top billing cases compare to subject area and Type of case?
- What law firms are high value and how do they compare to top billers and category?

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Acknowledgments
The data used in this analysis was generated on October 16, 2024. Special thanks to team member Christopher for his support in data collection and initial exploration.

---

Feel free to contribute, open issues, or suggest improvements!
