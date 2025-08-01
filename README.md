
# Project 1: Non-Majors Computing Survey Analysis

**Author:** Aidan Qadi  
**Date:** August 1, 2025

## Purpose

This project analyzes survey responses from non-major students who enrolled in computing courses at County College of Morris (CCM) to inform and improve recruiting and messaging by the CCM IT Department. Using both the original and cleaned survey data, the analysis answers four core questions:
1. What motivates non-majors to take computing classes, and how do those motivations vary by age and gender?  
2. Which information sources most effectively reach enrolled non-major computing students?  
3. Is there a relationship between how students heard about CCM and their interest in taking additional computing classes?  
4. Which specific computing subjects (e.g., web development, cybersecurity, AI) are of greatest interest, and how does that vary by race/ethnicity?

## Repository Structure / Contents

- `data/raw/NonMajorSurvey.csv`  
  The original uncleaned survey data as provided. Contains raw responses including demographic fields (e.g., Gender, Race/ethnicity, Age), checkbox-style motivations, source attribution, and interest indicators. The raw file is the starting point for all cleaning and analysis; it contains 92 responses and no exact duplicate rows.

- `data/cleaned/cleaned_non_majors_survey_final (3).csv`  
  The cleaned and standardized version of the survey. Key transformations applied (and documented in the cleaning notebook) include:
  - Standardized, shortened, and normalized column names for readability.  
  - Checkbox / "Yes"/"No"/"Don't recall" responses mapped to binary indicators (with "Don't recall" treated as lack of confirmed exposure).  
  - Overall interest score converted to numeric.  
  - Demographic text fields (gender, race_ethnicity, age) trimmed and normalized.  
  - Duplicate checking was performed: the original raw dataset had no duplicates; the cleaned version contains one exact duplicate row (not removed, with the rationale documented in the cleaning notebook).  

- `notebooks/Project1_NonMajors_Cleaning.ipynb`  
  Notebook documenting the data cleaning phase. Includes:
  - Exploration of raw value distributions (e.g., value_counts for demographics, motivations, information sources).  
  - Explicit documentation of cleaning decisions and rationale (e.g., why responses were recoded, how column names were renamed).  
  - Before-and-after comparisons where applicable.  
  - Handling of potential duplicates and explanation of decisions around them.

- `notebooks/Project1_NonMajors_Analysis_Fixed_executed.ipynb`  
  Analysis notebook built on the cleaned data. Contains:
  - Environment/version reporting and data import.  
  - Answers to the four research questions with appropriate grouping (by gender, age, race/ethnicity, source).  
  - Visualizations (bar charts, boxplots, heatmap-style plot) with captions and comparisons.  
  - Aggregated summaries (counts/proportions) and demographic breakdowns.  
  - A summary of findings to guide messaging/recruitment strategy.

- `load_nonmajor_survey.py` *(optional utility)*  
  A helper script to interactively load the survey CSV in Jupyter or Colab. It attempts to auto-load the expected file, falls back to Colab's uploader, then to a widget, and finally to a manual path prompt.

- `README.md`  
  This file. Explains the project's purpose, contents, usage, and key findings.

- `requirements.txt` *(recommended)*  
  (If present) Lists the specific versions of Python libraries used (e.g., pandas, numpy, matplotlib) to aid reproducibility.

## Key Findings (draft / to be finalized)

- **Motivations:** Career advancement and maintaining current computing skills are among the most common reasons students take computing classes. Demographic differences (by gender and age) suggest opportunities to tailor messaging.  
- **Sources:** Some channels (e.g., institutional website or guidance counselors) reach more students; certain sources correlate with higher expressed interest in further computing study.  
- **Interest Correlation:** How a student first heard about the course is associated with their likelihood of wanting more computing classes, indicating that higher-engagement channels can be prioritized.  
- **Subject Preferences:** Subjects like web development and cybersecurity show strong overall interest, with variation across race/ethnicity groups that can inform course offering decisions.

*(Fill in the exact numerical and qualitative nuances after reviewing the plots and tables in the analysis notebook.)*

## Reproducibility

- The notebooks print key library versions for transparency.  
- Data is organized under `data/raw` and `data/cleaned`.  
- To reproduce the analysis: clone the repo, install dependencies (e.g., from `requirements.txt`), and open/run the notebooks in Jupyter or Colab.

## Contact

Aidan Qadi  
