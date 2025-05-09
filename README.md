# 💊💉 Diabetes Dataset Analysis in R
This project performs exploratory data analysis and preprocessing on the Pima Indians Diabetes Dataset using R and the tidyverse ecosystem, with some additional visualizations and normalization via the caret package.

##📂 Dataset
The dataset used is diabetes.csv, which includes 768 observations and 9 variables related to medical predictors and a binary target outcome (diabetes diagnosis).

Variables:
Pregnancies: Number of times pregnant

Glucose: Plasma glucose concentration

BloodPressure: Diastolic blood pressure (mm Hg)

SkinThickness: Triceps skin fold thickness (mm)

Insulin: 2-Hour serum insulin (mu U/ml)

BMI: Body mass index

DiabetesPedigreeFunction: Diabetes pedigree function

Age: Age in years

Outcome: Diabetes presence (1) or absence (0)

##📊 Analysis Steps
1. Data Loading & Overview
Read CSV file into a data frame

Preview first rows with head()

Inspect structure using glimpse()

Get summary statistics with summary()

Check column names with colnames()

2. Visualization
Bar plot showing diabetes diagnosis distribution (Outcome 0 vs 1)

Age analysis: Frequency count for ages occurring more than 10 times

Boxplot visualizing Insulin vs BloodPressure, grouped by Glucose (note: the facet_grid might require correction)

3. Data Transformation
Convert Outcome to a factor (categorical variable)

Normalize features using caret::preProcess method = "range"

Recoded outcome levels: "NO" and "YES"

4. Correlation Analysis
Compute and visualize correlation matrix of the 8 predictor variables using corrplot

##📦 Dependencies
Make sure to install/load the following R packages:

r
Copiar
Editar
library(tidyverse)    # Data wrangling and visualization
library(caret)        # Preprocessing and ML utilities
library(corrplot)     # Correlation heatmap
library(ggplot2)      # Additional plotting
You can install them using:

r
Copiar
Editar
install.packages(c("tidyverse", "caret", "corrplot"))

##📈 Output Metrics
After preprocessing, the proportion of outcomes:

NO (non-diabetic): ~65.1%

YES (diabetic): ~34.9%
