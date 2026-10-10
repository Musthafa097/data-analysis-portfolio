# British Airways Customer Booking Prediction

## Project overview

This project uses customer booking data to explore whether a customer is likely to complete a holiday booking. The aim is to help British Airways identify potential customers earlier and make better-informed marketing decisions.

## What I did

1. Explored and prepared a customer booking dataset with 50,000 records.
2. Converted text categories into model-ready features.
3. Trained a Random Forest model to predict `booking_complete`.
4. Evaluated it with 5-fold cross-validation.
5. Reviewed feature importance and summarised the findings in a slide.

## Cross-validation results

| Measure | Average result |
|---|---:|
| Accuracy | 85.2% |
| Precision | 51.7% |
| Recall | 12.6% |
| F1 score | 20.2% |
| ROC-AUC | 77.7% |

The data is imbalanced: about 15% of records are completed bookings. So, although accuracy is high, recall shows that the model identifies only about 13 out of every 100 customers who actually book. It would need improvement before it could be useful for targeting.

In this model run, route had the highest feature importance, followed by booking origin and purchase lead. Feature importance describes how much the model relied on a variable; it does not show that the variable causes a booking. Route has many distinct values, so its importance should be checked with additional methods.

## Files

- `booking_prediction.ipynb` — data preparation, model training, evaluation, and feature-importance chart.
- `model_summary.pptx` — a one-slide summary of the findings.
- `customer_booking.csv` — the dataset used for analysis; it is not included here. Obtain the permitted dataset separately and place it beside the notebook.

## How to run

1. Install Python and Jupyter Notebook.
2. Install `pandas`, `numpy`, `scikit-learn`, and `matplotlib`.
3. Place `customer_booking.csv` beside the notebook.
4. Open `booking_prediction.ipynb` and run the cells from top to bottom.

The results can vary if the data, preprocessing, model settings, or evaluation method changes. This is a learning project, not a production BA system.
