# British Airways Customer Booking Prediction

## Project overview

This project uses customer booking data to explore whether a customer is likely to complete a holiday booking. The aim is to help British Airways identify potential customers earlier and make better-informed marketing decisions.

## What I did

1. Explored the customer booking dataset and reviewed its columns and values.
2. Prepared the data for machine learning, including converting text categories into model-ready values.
3. Trained a Random Forest classification model to predict `booking_complete`.
4. Evaluated the model using 5-fold cross-validation and several performance measures.
5. Reviewed feature importance to see which inputs the model relied on most.

## Results

The average cross-validation results were:

| Measure | Result |
|---|---:|
| Accuracy | 85.2% |
| Precision | 51.7% |
| Recall | 12.6% |
| F1 score | 20.2% |
| ROC-AUC | 77.7% |

Although accuracy was 85.2%, the model found only about 13 out of every 100 customers who completed a booking (recall). This means the model may miss many potential bookers, so it needs further improvement before being used for customer targeting.

In this model run, route had the highest feature importance, followed by booking origin and purchase lead. Feature importance describes how much the model relied on an input; it does not show that the input causes a booking.

## Files

- `British_airways.ipynb` — the detailed, guided notebook with data exploration, feature preparation, model evaluation, and feature-importance visualisation.
- `booking_prediction.ipynb` — a second, streamlined version of the analysis.
- `model_summary.pptx` — a one-slide summary of the model and findings.
- `customer_booking.csv` — the dataset used by the notebook (keep this out of the repository unless you have permission to share it).

## How to run

1. Install Python and Jupyter Notebook.
2. Install the packages used in the notebook, such as `pandas`, `scikit-learn`, `matplotlib`, and `seaborn`.
3. Place the permitted dataset file beside the notebook, or update the notebook's data path.
4. Open either notebook and run it from top to bottom.

The exact results may vary if the data, preprocessing, train/test split, or model settings change.

## Limitations and next steps

- The low recall means the current model misses many customers who complete bookings.
- Test a different prediction threshold and evaluate the precision/recall trade-off.
- Compare feature importance with a method such as permutation importance, particularly because route has many distinct values.
- If available and appropriate, explore additional customer-related information and validate the model on newer data.

## Note

This is a learning project based on the British Airways Data Science virtual experience. It is not an operational BA booking system or a production-ready model.
