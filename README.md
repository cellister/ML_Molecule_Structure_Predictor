# Machine Learning Molecule Structure Predictor: Perovskite Classification

This project was completed as the final Phase 3 assessment in the Flatiron School’s Data Science Bootcamp. 

Analysis by Erin Wasserman, April 2024

# Overview

# Business Problem

A Research Laboratory has asked for an analysis of a dataset to help understand the relationships between various physical and chemical properties of perovskite materials and their crystal structure types.

This project will determine:

(1) If there are any discernable patterns or correlations among the different variables and perovskite structure types?
(2) How well features like the Glodschmidt tolerance factor, the electronegativity, and octahedral factor contribute to the predictive accuracy of the classification model? 
(3) Are there any limitations or challenges in interpreting the model's predictions based on the selected features? 

# Data Understanding

**Dataset Description**

[Kaggle Crystal Structure Dataset] (https://www.kaggle.com/datasets/meetnagadia/crystal-structure-dataset/data). Each record represents a different Perovskite structures based on their characteristics. The data consists of 4,165 ABO3 perovskite-type oxides. Each observation is described by 13 feature columns and 1 class column which identifies it to be either a cubic, tetragonal, orthorhombic, and rhombohedral structure.

**Data Features**

List of Feature (or attributes, either work) Descriptions

vA : Valence of A
vB : Valence of B
r_A6 : ionic radius of A cation (A6)
r_A12 : ionic radius of A cation (a second one, A12)
r_B6 : ionic radius of B cation
EN_A : Average electronegativity value of A cation
EN_B : Average electronegativity value of B cation
bond_len_AO : Bond length of A-O pair
bond_len_BO : Bond length of B-O pair
ENR_diff : Electronegativity difference with radius
tG : Goldschmidt tolerance factor
tau : New tolerance factor
mu : Octahedral factor

**Data Splits**

-The dataset was randomly split into training (80%) and test (20%) sets to evaluate model performance.
-Kfold Stratified crossvalidation was use to ensure that each class of the target variable is represented proportionally in each split.

**Data Quality Issues**

-No significant data quality issues were identified in the dataset.
-Nonphysical data was identified and removed using domain knowledge.

**Data Licensing and Usage**

-[Database: Open Database, Contents: Copyright Original Authors](https://opendatacommons.org/licenses/odbl/1-0/)


# Methodology

## Data Preparation

**Data Cleaning and Preprocessing**
-Missing values and placeholders were identified and removed from the dataset.
-Histograms, Correlation Plots, and Pair plots were used to inform data cleaning.

## Modeling

-Decision Tree
-Random Forest
-Support Vector Machine

# Evaluation

-Kfold Cross-validation
-Accuracy
-Comparison Table

## Limitations

-More detailed explanation of the feature variables would have maximized the data cleaning.
-An accruacy of 100% was not achieved.

# Key Findings

## Decision Tree

* Accuracy score
* Top three feature importance

## Random Forest

* Accuracy score
* Top three feature importance

## Support Vector Machine

* Accuracy score
* Top three feature importance

## Actionable Insight

<ol>
<li> More steps should be taken to improve the accuracy, which can be done by exploring more models.
<li>Instead of training all models individually, I may explore ensemble methods that combine predictions from multiple models.

Ensemble methods include: bagging boosting stacking

These can lead to improved performance compared to individual models. In this case, I might focus on training a diverse set of base models to use in the ensemble.

</ol>

## Next Steps

While providing valuable insights, the analysis acknowledges the need for further investigation to address nuances and ensure a comprehensive understanding of categorizing Perovskite Crystal Structures.
<ol>
<li> Different crystal structures of perovskite materials can exhibit unique properties that make them suitable for specific applications. Knowing the researcher's goals could help optimize the data for that purpose.

<li>How do bond lengths relate to the 'lowest distortion' classification? 

<li>What insights can be gained from analyzing the relationships between features in the context of target perovskite crystal structures? 

<li> Can the model's predictions be interpreted in terms of the underlying chemical and structural properties represented by these features?

<li>Are certain atoms susceptible to false positives within the parameters of the different models?
    
</ol>
These next steps aim to address identified inconsistencies, enhance the robustness of the analysis, and provide more actionable insights for the researcher's decision-making processes.

# Author

Name: Erin Wasserman

GitHub: [Cellister](https://github.com/cellister)

Email address: cellister at gmail .com

#Repository Structure

* **Jupyter Notebook**

The [Jupyter Notebook](https://github.com/cellister/Film-Investment-Analysis-Project/blob/main/Film_Investment_Analysis_Notebook.ipynb) is the key deliverable and contains the details of my data strategy, methodology, data cleaning, visualizations, and actionable insights.

* **Presentation**

This 5-7 minute, non-technical [presentation](https://github.com/cellister/Film-Investment-Analysis-Project/blob/main/Report%20PDFs/Erin_Wasserman_presentation_PDF_P2.pdf) was made in [Canva](https://www.canva.com/design/DAFzlcctuzo/YpMIvURJO6cI7aveTLrNDA/edit?utm_content=DAFzlcctuzo&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton) and gives an impactful and brief overview of the key insights and recommendations. 

* **Data**

The data used in this analysis can be found in the ‘Data’ folder. Some data can be found on the [Kaggle Dataset](https://www.kaggle.com/datasets/meetnagadia/crystal-structure-dataset/data).

```

├── Photos
│   ├── genre_analysis
│   ├── notebook
│   ├── profit_analysis
│   ├── release_date_analysis
│   └── runtime_analysis
├── Data
├── Project PDFs
│   ├── film_investment_analysis_presentation.pdf
│   ├── film_investment_analysis_notebook.pdf
│   └── github_repository.pdf
├── .gitignore
├── Film_Investment_Analysis.ipynb
└── README.md
```


