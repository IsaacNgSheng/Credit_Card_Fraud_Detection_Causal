# Credit_Card_Fraud_Detection_Causal

## Project Overview

This project explores the causal relationships and predictive factors associated with credit card payment defaults. Using econometric modeling, instrumental variable (IV) analysis, and machine learning techniques, such as causal forests, the study aims to uncover the drivers of credit card fraud and provide actionable insights for financial institutions.

## Goals

1. Understand the causal impact of key variables on default probabilities.
2. Provide data-driven recommendations for mitigating credit risk.

## Dataset

The project uses the Credit Card Fraud Detection Dataset from Kaggle, which contains 164 attributes reflecting socio-economic factors, financial stability, and established industry practices.
Dataset URL:
https://www.kaggle.com/datasets/mishra5001/credit-card/data

## Project Timeline

The project begun with Project_Proposal.pdf, before continuing with the presentation (both Presentation_Code.Rmd and Project_Presentation.pptx), finally ending off with the overall project (both Project_Post_Presentation.Rmd and Causal_Project.pdf)

1. Project_Proposal.pdf
2. Presentation_Code.Rmd and Project_Presentation.pptx
3. Project_Post_Presentation.Rmd and Causal_Project.pdf

## Methodology

### Data Preprocessing

- Dimensionality reduction using stepwise selection and multicollinearity checks.
- Final selection of key variables: AMT_ANNUITY, AMT_CREDIT, and AMT_GOODS_PRICE

### Econometric Analysis

- Developed a two-stage regression model with AMT_ANNUITY as the main independent variable and TARGET (default indicator) as the dependent variable.
- Conducted IV analysis:
  - Identified AMT_GOODS_PRICE as the strongest IV based on correlation and validity tests.
  - F-statistic and Wu-Hausman tests confirmed instrument strength and minimal endogeneity.

 ### Causal Forest

- Built a Bayesian Causal Forest (BCF-IV) model to analyze heterogeneous treatment effects.
- Derived insights into the varying impact of AMT_ANNUITY on default probability across subgroups.

### Counterfactual Analysis

Estimated default probabilities under hypothetical changes in key variables (e.g., doubling AMT_ANNUITY).

## Results

### Key Findings

- Econometric Model: A unit increase in AMT_ANNUITY has a minimal yet significant effect on default probability.
- Heterogeneous Effects: Subgroups with differing income levels and family sizes show varied responses to changes in AMT_ANNUITY.
- Counterfactuals: Doubling AMT_ANNUITY increases default probability for certain borrowers, suggesting financial stress from higher repayment burdens.

### Variable Importance:

The causal forest identified critical predictors such as:
1. AMT_INCOME_TOTAL
2. AMT_CREDIT
3. EXT_SOURCE_2

### Insights for Financial Institutions

- Customize loan products for sensitive subgroups.
- Enhance KYC processes by focusing on influential variables.
- Use advanced causal models to improve fraud detection and risk mitigation.

## Setup and Usage

1. Clone the Repository:
git clone https://github.com/IsaacNgSheng/Credit_Card_Fraud_Detection_Causal.git
cd Credit_Card_Fraud_Detection_Causal

2. Open the R Markdown files in your R IDE (e.g., RStudio):
Presentation_Code.Rmd
Project_Post_Presentation.Rmd

3. Install necessary R packages listed in the .Rmd files.

4. Render the .Rmd files to run the analysis and generate outputs.
