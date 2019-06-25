# Exoplanet Exploration

To predict correct clasification of exoplanets, I used the following models:
 1. SVC from sklearn with linear kernel, and achieved a 85% score on training data, and 84% score on test data
 2. I used GridSearch to find the best hyperparameters for SVC, which were identified to be C=50 and gamma=0.0001. With these parameters the training score was 89% and test score 88%
 3. Random Forest classifiers with n_estimators=200 and n_estimators=1000 achieved similar accuracy of 89.5%
 4. Before tuning, the logistic regression achieved accuracy of 83%, and after using the GridSearch on C value and penalty type, the accuracy improved to 87% with C=50 and penalty='l1'
 
 
 Precision and Recall remain low in all models, particularly:
 1. low precision for CONFIRMED exoplanets. This means there are a many false positives
 2. low recall on CANDIDATE exoplanets, which means that many were missed
 
 Conclusion: different models achived similar accuracy with Random Forest giving the best accuracy of 89.5%
