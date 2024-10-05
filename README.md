# MVTS_Opioid
Predictive Model for Opioid Relapse Risk Using Multivariate Time-Series (MVTS) Drug Usage Data

## Overview
This project builds upon previous work led by Prof. Sean Luo, titled ["Individual-Level Risk Prediction of Return to Use During Opioid Use Disorder Treatment"](https://jamanetwork.com/journals/jamapsychiatry/fullarticle/2810311) published in _JAMA Psychiatry (2023)_. Unlike the original study, which focused on predicting whether patients are likely to relapse within a 12-week treatment period, this project aims to predict the risk score of return-to-use at any given time point. This transforms the problem from a one-time prediction task into a time-series forecasting challenge, thereby introducing more complexity.

## Data source
The dataset used for the project is [CTN-0094](https://github.com/CTN-0094/public.ctn0094data?tab=readme-ov-file), which has been harmonized from three of the largest clinical trials on medication-assisted opioid treatment: **CTN-0027**, **CTN-0030**, and **CTN-0051**.

## Pipelines
This repository contains two separate pipelines:
- (partial) **Reimplementation of OUD predictive model in Python**:

  The original predictive model, initially implemented in R, has been reimplemented in Python based on the publicly available data and the descriptions provided in the JAMA paper. The original model used logistic regression; in this study, random forest showed slightly better performance compared to logistic regression. Data processing, modeling, visualization, analysis, as well as the requirement of necessary Python libraries are all included in the Jupyter Notebook.
- **MVTS Opioid Relapse Risk Prediction/Forecasting Pipeline**:

  A new pipeline was developed to tackle the multivariate time-series forecasting task. Given the **irregularities in drug usage data**, a **long short-term memory (LSTM) model** was implemented to capture the complex patterns found in both the time-series data and static features (e.g., demographic information) to predict relapse risk more effectively. I am also exploring the potential improvement by replacing the general LSTM model with the latest revisited LSTM model ([minLSTM](https://arxiv.org/abs/2410.01201)) and lite version Transformer architecture.

## Technical support and bug report
The Jupyter Notebook containing the code for the OUD predictive model can be found in the `OUD_pred` folder. The MVTS forecasting pipeline is not published and is intended to remain private; therefore, its code is not available in this repository.

If you wish to preview the code of the MVTS forecasting pipeline (in Jupyter Notebook format) or report any bugs related to the OUD predictive model, please contact [Le Li](mailto:lile.moziya@gmail.com). 
