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

### Representation

| |0|1|
|-|-|-|
|__0__| TN | FP |
|__1__| FN | TP |

The horizontal axis corresponds to the predicted values(`y-predicted`) and the vertical axis correspomds to the actual values(`y-actual`).

+ __[1][1]__ represents the values which are predicted to be false and are actually false.
+ __[1][2]__ represents the values which are predicted to be true, but are false.
+ __[2][1]__ represents the values which are predicted to be false, but are true.
+ __[2][2]__ represents the values which are predicted to be true and are actually true.

### Using Confusion Matrix in code

Confusion Matrix can be used in python by importing the `metrics` module from `sklearn`.

```python
from sklearn import metrics
cm = metrics.confusion_matrix(y_actual, y_predicted)
```

We can calculate the rate of success as:-

r = (TN+TP)/(FN+FP)

It can be directly interpreted by,

```python
print("Accuracy = ",metrics.accuracy_score(y_actual, y_predicted)*100)
```
