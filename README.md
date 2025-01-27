<br />
<div align="center">
      <img src="https://media.istockphoto.com/id/1668413951/pt/vetorial/mosquito-biting-on-human-skin-stock-illustration.jpg?s=612x612&w=0&k=20&c=smwy0Gzyoqd3QNVvrV0dQU3cQug_ekSC1W5TguwPBM0=" width=400 />
  </a>
  <h1 align="center">Dengue Case Analysis and Death Prediction in Brazil (2024)</h1>
</div>
<br>

## About The Project
This project addresses one of Brazil's most significant public health challenges: dengue fever. With the rising number of cases in 2024, understanding and predicting patient outcomes has become increasingly crucial for healthcare planning and resource allocation.

### Problem Statement
Dengue fever, transmitted primarily by the Aedes aegypti mosquito, affects millions worldwide, with Brazil being particularly impacted due to its tropical climate and urban conditions. While many dengue infections are asymptomatic or mild, some cases can progress to severe forms like hemorrhagic fever and dengue shock syndrome, which can be fatal.

### Project Goals
- Analyze dengue case patterns across Brazil in 2024
- Develop accurate predictive models for patient mortality
- Identify key factors contributing to severe cases
- Provide insights for healthcare resource allocation
- Support public health decision-making

### Key Features
- Comprehensive analysis of patient demographics and clinical data
- Seasonal pattern analysis of dengue cases
- Geographic distribution analysis (capital vs. interior regions)
- Machine learning models for mortality prediction
- Performance evaluation using multiple metrics

## Contributor
https://github.com/LeonardoIshida

## Overview
The project utilizes data from SINAN (Sistema de Informação de Agravos e Notificação) to analyze dengue cases and develop predictive models for patient outcomes. Our analysis covers various aspects including demographic data, socioeconomic context, medical history, and public health indicators.

## Dataset Information
The dataset can be found in this [link](https://www.kaggle.com/datasets/henriquerezermosqur/dados-sus-sinan-dengue-2021-2024), and includes:
- Patient demographic information
- Clinical symptoms and diagnoses
- Treatment details
- Geographic location data
- Temporal information
- Outcome data (survival/mortality)

## Models Implemented
Three different classifiers were evaluated:
- Light Gradient Boosting Machine (LGBM)
- Random Forest
- Multi-Layer Perceptron (MLP)

## Results
All models achieved high accuracy, with MLP showing the best overall performance:

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|---------|-----------|
| LGBM | 0.99 | 0.70 | 0.89 | 0.78 |
| Random Forest | 0.99 | 0.73 | 0.92 | 0.81 |
| MLP | 0.99 | 0.81 | 0.99 | 0.87 |

## Data Preprocessing
### Cleaning Steps
- Handled missing values using specific imputation methods based on SUS documentation
- Removed columns with excessive missing data (>70% missing)
- Removed duplicate entries
- Eliminated constant-value columns

### Feature Engineering
- Transformed categorical variables using Label Encoding
- Normalized numerical features using Standard Scaler
- Created new features:
  - Season of the year (based on notification date)
  - Interior/Capital classification (based on IBGE city codes)
  - Temporal features from dates

## Dependencies
- Pandas: Data manipulation and analysis
- NumPy: Mathematical operations and array manipulation
- Altair: Data visualization
- Scikit-learn: Machine learning models and preprocessing
- LightGBM: Gradient boosting framework

## Model Parameters
### LGBM
- n_estimators: 10
- max_depth: 3
- min_child_samples: 2
- reg_alpha: 0.1
- reg_lambda: 0.1

### Random Forest
- n_estimators: 50
- max_depth: 10
- min_samples_split: 5
- min_samples_leaf: 2
- max_features: sqrt

### MLP
- hidden_layer_sizes: (50)
- activation: tanh
- alpha: 0.3
- max_iter: 100

## Future Work
- Explore additional machine learning techniques (SVM, CNN)
- Investigate the impact of different preprocessing methods
- Evaluate model performance across different regions of Brazil
- Incorporate external data (climate, socioeconomic factors)

## Acknowledgments
This project was developed under the supervision of Prof. Roseli Aparecida Francelin Romero at the Institute of Mathematical and Computer Sciences (ICMC) - University of São Paulo.

