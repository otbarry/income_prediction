# **Income Predictions: A Census Snapshot**

## **Data**
- The data was extracted from the Census Bureau database by Ronny Kohavi and Barry Becker (Data Mining and Visualization, Silicon Graphics).
- It contains demographic and occupational information such as employment status, number of years of education, and marital status.
- The prediction task is determining whether someone makes over or under $50K a year.

## **ML Techniques used**
- Used recursive and sequential feature selection
- Performed grid and random search for hyperparameter tuning
- Implemented SVM, logistic regression, random forest and KNN models
- Evaluated using cross-validated balanced accuracy for each strategy
- Tried a hard voting  and a stacking classifier using all models above to improve performance

## **Key Insights**
- The top 5 features for predicting the income bucket were being married to a civilian, years of education, the hours worked per week, being an executive or manager, the weights set to generalize the census results, and being self employed.
- The stacking model has an AUC of 0.89 indicating that the model can effectively distinguish between income buckets.
- The stacked model model identifies low earners better than individuals with a higher income range ( not surprising as the dataset contains more records in the lower income range and only 25% of high earners).
- The models ranked by order of balanced accuracy on the test set are in the following order: logit(75.77), knn(75.43), svc(75.37), stacking classifier(75.12), random forest(75.02), voting classifier(73.94).
- In terms of accuracy, the models are ranked as follows:random forest (85.48),voting classifier(84.87), stacking classifier (84.83), svc(84.44), logit (84.17), knn (83.33).
- Therefore the model with the higher balanced accuracy on the test set is the logit model and the model with the highest accuracy is the random forest.
