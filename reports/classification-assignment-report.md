# Classification Assignment: Predicting Premium House Listings

## Classification Question

The goal of this project was to predict whether a house should be classified as
a premium listing. A house was labelled premium when its sale price was at least
$1,000,000. The classifier used sqft_living and yr_built as predictor
variables.

The original price variable was not used as a model input because the premium
label was derived from price. Including it would create target leakage.

The dataset contained 4,207 regular houses and
344 premium houses. Premium houses represented approximately
7.6% of the data.

## Metric Optimised

I used F1 score as the main evaluation metric.

Accuracy alone would not be enough because the classes are imbalanced. A model
could obtain high accuracy simply by predicting the more common regular class.
That model could still miss many premium houses, as shown by the baseline
classifier, which scored 0.924 accuracy but 0.000 F1.

F1 combines precision and recall. Precision measures how often houses predicted
as premium are actually premium, while recall measures how many real premium
houses the model successfully identifies.

## Model Results

The selected model was Random Forest.

Its test-set performance was:

- Accuracy: 0.894
- Precision: 0.379
- Recall: 0.638
- F1 score: 0.476
- ROC-AUC: 0.882

## Business Interpretation

Random Forest is the model I would trust more for this task. It achieved a higher F1 score (0.476) than Logistic Regression (0.439), with precision of 0.379 and recall of 0.638. Random Forest can capture non-linear relationships and interactions between sqft_living and yr_built that a linear decision boundary cannot, which better separates premium houses from regular ones.