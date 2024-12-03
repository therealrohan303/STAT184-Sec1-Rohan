# Introduction
This repository explores potential gender biases in UC Berkeley’s admissions process using the 1973 dataset provided for analysis. The goal was to evaluate whether gender played a significant role in admission outcomes, as per the plaintiff's claim in a lawsuit. The dataset includes information about applicants, their gender, admission decisions, and the majors they applied to. The findings are documented in a Quarto notebook.

# Implementation
The analysis was performed using R with the following steps:
- Data Preparation: Imported the dataset from a public source and reviewed its structure for completeness.
- Exploratory Data Analysis (EDA): Grouped the data by gender and major to calculate admission rates.
- Visualization: Generated bar plots to highlight trends in admission rates across gender and majors.
- Challenges and Solutions: Addressed missing values by verifying dataset integrity and resolved grouping issues by leveraging dplyr functions effectively.
  
Below is a sample of the R code used for visualization:

ggplot(admission_rates_gender_major, aes(x = Major, y = Admission_Rate, fill = Gender)) +
  geom_bar(stat = "identity", position = "dodge") +
  labs(title = "Admission Rates by Major and Gender", x = "Major", y = "Admission Rate") +
  theme_minimal()
