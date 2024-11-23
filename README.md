# Hybrid RF/FSO Communication: Predictive Modeling for Link Attenuation Using Machine Learning

## Project Overview

This project focuses on enhancing the reliability of hybrid Radio Frequency (RF) and Free-Space Optical (FSO) communication systems by developing machine learning models to predict channel attenuation under various weather conditions. The increasing congestion of the RF spectrum necessitates alternative communication methods, and hybrid RF/FSO systems offer a promising solution by combining the robustness of RF with the high data rates of FSO. However, these systems are highly susceptible to adverse weather conditions that can lead to significant link attenuation.

## Objectives

- **Develop predictive models** using Random Forest Regressors to estimate channel attenuation in hybrid RF/FSO systems.
- **Optimize model performance** through feature selection, hyperparameter tuning, and model evaluation.
- **Compare specific models** tailored to individual weather conditions with generic models encompassing all conditions.
- **Identify key meteorological features** that significantly impact channel attenuation.

## Dataset

- **Synthetic dataset** comprising over 91,000 entries.
- **Meteorological parameters** include absolute humidity, particulate matter concentration, rain intensity, relative humidity, temperature, visibility, wind direction, and wind speed.
- **Weather conditions** represented by SYNOP codes ranging from 0 to 8 (e.g., clear skies, dust storms, fog, drizzle, rain, snow, showers).
- **Data structure** designed as a time series to capture seasonal variations and patterns.

## Methodology

1. **Exploratory Data Analysis (EDA):**
   - Identified correlations among features and their relationship with channel attenuation.
   - Visualized data distributions and highlighted potential issues like multicollinearity and dataset imbalance.

2. **Model Selection and Evaluation:**
   - Chose Random Forest Regressors due to their robustness and ability to handle high-dimensional data.
   - Evaluated models using Root Mean Square Error (RMSE) and Coefficient of Determination (R²).

3. **Feature Selection:**
   - Employed an iterative feature elimination method based on Mean Decrease in Impurity (MDI).
   - Performed feature selection separately for each weather condition and for the generic model.

4. **Hyperparameter Tuning:**
   - Used Randomized Search Cross-Validation to optimize hyperparameters like the number of estimators, maximum depth, and minimum samples required for splits and leaf nodes.

5. **Model Comparison:**
   - Compared specific models for individual weather conditions against a generic model trained on the entire dataset.
   - Analyzed performance improvements and identified key features for each condition.

## Key Findings

- **Specific models** tailored to individual weather conditions outperformed generic models, particularly under adverse conditions like dust storms and fog.
- **Significant features** affecting attenuation included visibility, particulate matter concentration, rain intensity, and humidity.
- **Random Forest models** effectively predicted channel attenuation, but may not fully capture temporal dependencies inherent in time-series data.

## Conclusion

The project demonstrates the effectiveness of using machine learning models, specifically Random Forest Regressors, to predict channel attenuation in hybrid RF/FSO communication systems. By focusing on condition-specific models and optimizing feature selection, the models achieved lower RMSE values, indicating more accurate predictions. These findings contribute to the development of more resilient communication systems capable of adapting to diverse and challenging weather conditions.

## Future Work

- **Incorporate real-world datasets** to validate and refine predictive models under actual atmospheric conditions.
- **Address dataset imbalances** through oversampling minority classes or sophisticated sampling methods.
- **Explore advanced algorithms** like gradient boosted trees (XGBoost, LightGBM, CatBoost) and deep learning models (RNNs, LSTMs) to improve predictive accuracy.
- **Implement feature selection techniques** such as Principal Component Analysis (PCA) and permutation importance.
- **Integrate model explainability tools** like SHAP values to gain deeper insights into feature impacts.

## Acknowledgements

Special thanks to the project supervisor, Siu Wai Ho, for guidance and support throughout this research.

## Contact Information

- **Author:** Shavin Tharinda Kaluthantri
- **Email:** [your.email@example.com](mailto:a1904121@adelaide.edu.au)
- **Affiliation:** School of Mathematical Sciences, University of Adelaide

---

*This project was submitted as part of the Data Science Research Project Part A at the University of Adelaide.*
