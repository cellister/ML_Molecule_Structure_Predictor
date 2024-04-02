# Machine Learning Molecule Structure Predictor: Perovskite Classification

This project was completed as the final Phase 3 assessment in the Flatiron School’s Data Science Bootcamp. 

Analysis by Erin Wasserman, April 2024

# Overview

This project explores different machine learning algorithms to predict the lowest distortion in perovskite structures, which is a critical aspect in ceramic science, materials physics, and solid-state inorganic chemistry. Researchers have identified a total of 73 elements in the A and B cation sites of ABO3 structures, leading to numerous oxides of the perovskite type.

The objective is to develop models capable of accurately classifying perovskite structures based on features such as electronegativity, ionic radius, valence, and bond lengths of A-O and B-O pairs, thereby aiding in the prediction and optimization of material properties. Model performance is assessed using the Accuracy Score metric.

# Business Problem

A Research Laboratory has asked for an analysis of a dataset to help understand the relationships between various physical and chemical properties of perovskite materials and their crystal structure types. Based on this analysis, the following recommendations are made:

- Utilize the Random Forest model.
- Enhance dataset with additional empirical data.
- Address missing values and discrepancies using insights from feature importance analysis to ensure data quality.
- Strategically target discrete values: Leverage RBF SVM's proficiency in capturing nonlinear relationships to target molecules with discrete values for improved predictive accuracy.

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

 Decision Tree Model: Identified significant features including 'tG', 'tau', 'ENR_diff', 'bond_len_BO', and 'EN_A'. 

Evaluation Scores:
Precision: 81%
Recall: 81%
Accuracy: 81%
F1-Score: 81%


## Random Forest

Random Forest Model: Highlighted 'tG', 'ENR_diff', 'tau', 'EN_B', and 'bond_len_AO' as important predictors.

Evaluation Scores:
Precision: 85%
Recall: 86%
Accuracy: 86%
F1-Score: 85%

## Support Vector Machine

RBF Support Vector Machine: Found 'tau', 'vA', 'vB', 'EN_B', and 'ENR_diff' as key features.

Evaluation Scores:
Precision: 83%
Recall: 83%
Accuracy: 83%
F1-Score: 82%

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

The [Jupyter Notebook](https://github.com/cellister/ML_Molecule_Structure_Predictor/blob/main/Project_PDFs/ML_Molecular_Structure_Predictor%20-%20Jupyter%20Notebook.pdf) is the key deliverable and contains the details of my data strategy, methodology, data cleaning, visualizations, and actionable insights.

* **Presentation**

This 5-7 minute, non-technical [presentation](https://github.com/cellister/Film-Investment-Analysis-Project/blob/main/Report%20PDFs/Erin_Wasserman_presentation_PDF_P2.pdf) was made in [Canva](https://www.canva.com/design/DAGAhemjCqQ/SC9XjPt87gS8cgYyPIWb5Q/edit?utm_content=DAGAhemjCqQ&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton) and gives an impactful and brief overview of the key insights and recommendations. 

* **Data**

The data used in this analysis can be found in the ‘Data’ folder. Some data can be found on the [Kaggle Dataset](https://www.kaggle.com/datasets/meetnagadia/crystal-structure-dataset/data).

```

├── Photos
│   ├── Other
│   ├── EDA
│   ├── SVM
│   ├── Random_Forest
│   └── Decision_Tree
├── Data
|   ├── Perovskite_train.csv
│   ├── Perovskite_test.csv
├── Project_PDFs
│   ├── ML_Molecule_Structure_Predictor.pdf
│   ├── ML_Molecule_Structure_Predictor.pdf
│   └── github_repository.pdf
├── .gitignore
├── ML_Molecule_Structure_Predictor.ipynb
└── README.md
```


