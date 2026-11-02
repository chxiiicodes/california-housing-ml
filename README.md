# california-housing-ml
Machine Learning project: California housing value prediction using Python and Random Forest.

# California Housing Price Prediction

## 1. Project Overview

This project explores supervised Machine Learning techniques to predict median house values across different geographic areas in California.

The main objective is to build, evaluate and compare regression models using Python and Scikit-learn, while understanding the complete Machine Learning workflow.

## 2. Dataset

The project uses the California Housing dataset provided by Scikit-learn.

* **Observations:** 20,640
* **Features:** 8
* **Target variable:** `MedHouseVal`

The target represents median house values per census block group, expressed in units of $100,000.

**Note:** Target values are capped at approximately $500,000. The dataset does not represent individual property prices.

## 3. Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## 4. Machine Learning Workflow

The project follows these steps:

1. Data loading and exploration.
2. Data preparation and splitting.
3. Linear Regression as a baseline model.
4. Random Forest Regressor.
5. Overfitting analysis.
6. Cross-validation.
7. Hyperparameter optimization using GridSearchCV.
8. Feature importance analysis using permutation importance.
9. Residual and prediction error analysis.
10. Final model evaluation on an independent test set.

## 5. Model Comparison

Two regression models were studied.

### Validation Results

Both models were evaluated on the same validation dataset.

| Model             |    MAE |   RMSE |     R² |
| ----------------- | -----: | -----: | -----: |
| Linear Regression | 0.5407 | 0.7339 | 0.6097 |
| Random Forest     | 0.3429 | 0.5250 | 0.8003 |

The Random Forest model achieved better validation performance than the Linear Regression baseline.

## 6. Hyperparameter Optimization

GridSearchCV was used with 5-fold cross-validation to optimize the Random Forest model.

Best parameters:

```python
{
    'n_estimators': 200,
    'max_depth': None,
    'min_samples_split': 2,
    'min_samples_leaf': 2
}
```

Best cross-validation R² score: **0.8012**.

## 7. Final Model Evaluation

After model selection, the Random Forest was retrained using the complete training dataset and evaluated on the previously untouched test dataset.

| Metric | Test Result |
| ------ | ----------: |
| MAE    |      0.3261 |
| RMSE   |      0.5040 |
| R²     |      0.8062 |

The final model achieved an R² score of **0.8062**, explaining approximately 80.62% of the variance in the target values on the test set.

The MAE corresponds to an average absolute error of approximately $32,605 in the dataset's target units.

## 8. Feature Importance

Permutation importance was used to estimate how much each feature contributes to the predictive performance of the trained model.

The most influential features were:

1. `MedInc` — Median income.
2. `Latitude` — Geographic latitude.
3. `Longitude` — Geographic longitude.
4. `AveOccup` — Average household occupancy.

These results highlight the importance of both socioeconomic and geographic information in predicting housing values.

## 9. Error Analysis

Residual analysis was conducted to examine the differences between actual and predicted values.

The analysis highlighted:

* Underestimation of some high-value observations.
* Overestimation of some lower-value observations.
* Residuals generally distributed around zero, without an obvious systematic pattern in the visual inspection.

## 10. Project Limitations

Several limitations should be considered:

* The dataset contains historical information.
* The target represents median values per geographic block, not individual property prices.
* Target values are capped at approximately $500,000.
* Random train/test splitting does not guarantee generalization to geographically independent regions.
* Feature importance does not establish causal relationships.
* The model is an educational project and is not intended for direct real-estate valuation.

## 11. Project Structure

```text
california-housing-ml/
│
├── README.md
├── california-housing-ml.ipynb
└── requirements.txt
```

## 12. Key Learning Outcomes

Through this project, I explored:

* Supervised Machine Learning.
* Regression models.
* Model evaluation metrics.
* Overfitting and generalization.
* Cross-validation.
* Hyperparameter optimization.
* Feature importance and permutation importance.
* Residual analysis.

## Author

Developed as part of my learning journey in Data Science, Machine Learning and quantitative methods.

**GitHub:** [chxiiicodes](https://github.com/chxiiicodes)

