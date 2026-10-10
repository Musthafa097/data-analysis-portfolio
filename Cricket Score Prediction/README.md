# IPL First-Innings Score Prediction

This project estimates the final first-innings score of an IPL match from the match situation partway through the innings. It is an educational machine-learning project, not an official IPL forecasting tool.

## How the prediction works

The notebook uses match details such as the batting team, bowling team, current runs and wickets, overs completed, and runs and wickets in the last five overs. The target is the innings' final total.

It compares several regression models, including Decision Tree, Linear Regression, Random Forest, Support Vector Regression, XGBoost, and K-Nearest Neighbours. It reports R-squared and error measures such as MAE, MSE, and RMSE, then uses a Random Forest model for example predictions.

## Files

- `IPL_Score_Predictor.ipynb` — data exploration, preparation, model comparison, and example predictions.
- `IPL score prediction report.docx` — written project report.
- `ipl_data.csv` — input dataset expected by the notebook; it is not included in this repository.

## Run the notebook

1. Open the notebook in Google Colab.
2. Get the IPL dataset used by the project and upload it when the notebook asks for `ipl_data.csv`.
3. Run the cells from top to bottom. If XGBoost is not available in the environment, install the `xgboost` package first.
4. Review the model scores and example predictions. The notebook saves the trained Random Forest as `ml_model.pkl`.

## Notes and limitations

- The predictions depend on the dataset, the teams represented in it, and the match state entered.
- The notebook evaluates models with one train/test split, so results can change with a different split. Cross-validation would give a more reliable comparison.
- The dataset is not included here. Add it only if you have permission to redistribute it.
- Team names and feature encoding should be checked before using the prediction function with new teams or data.
