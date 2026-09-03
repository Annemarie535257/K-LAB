# Classifier Project: Predicting Premium House Listings

## Dataset and Target

This project reuses the cleaned dataset from
`data/processed/house_prices_cleaned_featured.csv`. A house is labelled
premium when its sale price is at least $1,000,000, using
sqft_living and yr_built as the only two predictor features. price itself
is excluded from the features because the target was derived from it.

The dataset contained 4,207 regular houses and 344
premium houses, so premium houses represented approximately 7.6%
of the data.

## Algorithms Compared

Five classifiers studied in class were trained and evaluated on the same
80/20 stratified train/test split:

- **Decision Tree**: Splits the data on one feature at a time using yes/no questions until it reaches a leaf that gives the prediction.
- **K-Nearest Neighbors**: Looks at the most similar houses in the training data, by distance, and lets them vote on the prediction.
- **Naive Bayes**: Estimates how likely each feature value is under each class and combines those likelihoods with Bayes' rule.
- **Support Vector Machine**: Finds the line that best separates the two classes in scaled feature space and checks which side a house falls on.
- **Gradient Boosting**: Combines many small decision trees built one after another, each correcting the errors left by the ones before it.

## Results

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---|---|---|---|---|
| Naive Bayes | 0.937 | 0.636 | 0.406 | 0.496 | 0.935 |
| K-Nearest Neighbors | 0.930 | 0.553 | 0.377 | 0.448 | 0.882 |
| Support Vector Machine | 0.831 | 0.295 | 0.884 | 0.442 | 0.928 |
| Gradient Boosting | 0.841 | 0.289 | 0.754 | 0.418 | 0.919 |
| Decision Tree | 0.791 | 0.257 | 0.928 | 0.403 | 0.918 |

F1 score was used to rank the models because the premium class is rare.
A model can reach high accuracy just by predicting "regular" for almost
every house, so precision and recall, and their balance in F1, are more
informative for this problem.

## Example Walkthrough

One house from the test set was used to compare how each algorithm reasons
about the same input:

- Decision Tree: predicted Regular (probability of Premium = 0.131)
- K-Nearest Neighbors: predicted Regular (probability of Premium = 0.000)
- Naive Bayes: predicted Regular (probability of Premium = 0.016)
- Support Vector Machine: predicted Regular (probability of Premium = 0.013)
- Gradient Boosting: predicted Regular (probability of Premium = 0.015)

True label for this house: Regular

## Conclusion

Naive Bayes is the classifier I would trust most for this task. It reached the highest F1 score (0.496) among the five algorithms tested, balancing how often its premium predictions were correct (precision) against how many real premium houses it found (recall). The weakest performer on this dataset was Decision Tree (F1 = 0.403).