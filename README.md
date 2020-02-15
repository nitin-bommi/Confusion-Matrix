# Confusion-Matrix

We want to predict some data using Classification in Machine Learning.

Let the classifier be SVM, Decision Tree, Random Forest, Logistic Rgression, and so on.

What are the observations?
In each classifier, we get both right as well as wrong predictions.

### Wrong predictions can again be categorized into:-
+ False Positive
+ False Negative

### False Positive (type I error)
When we predict that something happens/occurs and it didn't happened/occured.(rejection of a true null hypothesis)
Example :- We predict that an earthquake would occur which didn't happen.

### False Negative (type II error)
When we predict that something won't happen/occur but it happens/occurs.(non-rejection of a false null hypothesis)
Example :- We predict that there might be no earthquake but there occurs an earthquake.

Usually, type I errors are considered to be not as critical as type II errors.

But in fields like Medicine, Agriculture, both the errors might seem critical.

A 2x2 matrix denoting the right and wrong predictions might help us analyse the `rate of success`. 
This matrix is termed the `Confusion Matrix`.
