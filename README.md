# Regularization: Buying Bias to Sell Variance

## Objective
I compared OLS, Ridge, and LASSO on a simulated high-dimensional dataset to see how penalized regression trades a small increase in bias for a large reduction in variance.

## Methodology
- Simulated a design with 200 predictors, of which only 5 had a true effect on the outcome, and 105 training rows.
- Fitted OLS, Ridge, and LASSO to the training data and compared their test MSEs.
- Traced the LASSO path to see the order in which predictors entered the model.
- Chose the LASSO penalty by 5-fold cross-validation, fitting the scaler inside every fold so no information from the validation fold leaked into training.
- Scored LASSO's selected variables against the known true predictors, counting true predictors found and false positives.
- Added two near-duplicate predictors and compared how LASSO and Ridge assigned weight between them.
- Wrote my own prompt asking an AI for the cross-validation loop, iterated on it, and checked its lambda and CV MSE against my own results.

## Key Findings
- **Test MSE:** OLS [YOUR VALUE], Ridge [YOUR VALUE], LASSO [YOUR VALUE].
- **LASSO path:** All five true predictors were in the model from step [YOUR VALUE]. The first noise variable entered at step [YOUR VALUE].
- **Cross-validation:** The chosen lambda was [YOUR VALUE], with a CV MSE of [YOUR VALUE].
- **Variable selection:** LASSO found [YOUR VALUE] of the 5 true predictors and selected [YOUR VALUE] false positives.
- **Near-duplicate predictors:** LASSO put [YOUR VALUE] on one predictor and zero on the other. Ridge split the weight [YOUR VALUE] and [YOUR VALUE].
- **AI-assisted cross-validation:** I went [YOUR VALUE] rounds with the AI. Comparing its lambda and CV MSE against mine: [YOUR RESULT].
