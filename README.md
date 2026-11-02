# california-housing-ml
Machine Learning project: California housing value prediction using Python and Random Forest.
# California Housing Price Prediction

## Project Overview

This project focuses on predicting median house values in California using supervised Machine Learning techniques.

The objective is to explore, train, evaluate and compare regression models using Python and Scikit-learn.

## Dataset

The California Housing dataset from Scikit-learn was used.

* Observations: 20,640
* Features: 8
* Target variable: `MedHouseVal`

The target represents median house values per census block group, expressed in units of $100,000.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Machine Learning Workflow

1. Data loading and exploration.
2. Data preparation and splitting.
3. Linear Regression baseline.
4. Random Forest Regressor.
5. Overfitting analysis.
6. Cross-validation.
7. Hyperparameter optimization using GridSearchCV.
8. Feature importance analysis using permutation importance.
9. Residual and error analysis.
10. Final evaluation on an independent test set.

## Models and Results

| Model                   |    MAE |   RMSE |     R² |
| ----------------------- | -----: | -----: | -----: |
| Linear Regression       | 0.5407 | 0.7339 | 0.6097 |
| Optimized Random Forest | 0.3261 | 0.5040 | 0.8062 |

The optimized Random Forest achieved an R² score of **0.8062** on the final test set.

## Feature Importance

Permutation importance highlighted the following features as particularly influential:

1. Median Income (`MedInc`)
2. Latitude
3. Longitude
4. Average Occupancy (`AveOccup`)

## Limitations

* The dataset contains historical information.
* The target represents median values per geographic block, not individual property prices.
* Target values are capped at approximately $500,000.
* Random train/test splitting does not guarantee generalization to geographically independent regions.
* The model is an educational project and is not intended for direct real-estate valuation.

## Project Structure

```text
california-housing-ml/
│
├── README.md
├── california_housing.ipynb
└── requirements.txt
```

## Author

Machine Learning project developed as part of my learning journey in Data Science and quantitative methods.
