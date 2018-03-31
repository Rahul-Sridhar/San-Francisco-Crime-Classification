# San Francisco Crime Classification

### **Description:** The main purpose of this project is to classify the category of crime based on Location and Time at which crime was commited .


The steps followed are as follows:
* Step-1: Download dataset from [https://www.kaggle.com/c/sf-crime/data](https://www.kaggle.com/c/sf-crime/data), store it in dataframe. 
* Step-2: Create a new dataframe containing Latitude, Longtitude, Category, Hour, Week, Month and Year of crime.
* Step-3: Create a new dataframe X by dropping Category. Create a variable Y containing the category of crime.
* Step-4: Split the data(X_train, y_train and X_test, y_test data(80:20)).
* Step-5: Check Different Machine Learning Algorithm to get best accuracy.
* Step-6: Check Different feature Engineering techniques on a particular algorithm(I have tried on KNN) to get better accuracy.
     * Convert to 3 Dimensional point(x, y, z) from Latitude and Longtitude and use as input.
     * Use only Latitude and Longtitude as input data.
     * Use Hour, Week, Month, Year, Latitude, Longtitude as input data.
     * Use the columns of dataframe that has positive correlation with category of crime.
     * Try on a smaller part of dataset maybe the model is overfitting.
* Step-7: Use One Hot Encoder Technique to submit predicted value into required submission format


# Conclusion
* Out of the feature engineering methods suggested the one which works best on KNN is simply by taking latitude and longtitude as input data.
* Since input data contains negative values we cannot use OVA Naive Bayes.
* OVA SVM with linear and rbf kernel and CrammerSVM 
* The  Algorithm gives the best accuracy of  for the given dataset.

|       Algorithm       |           Parameters           | Accuracy |
|:----------------------|:------------------------------:|:--------:|
|          KNN          |              K= 50             |  27.65%  |
|    OVA Naive Bayes    |               -                |    -     |      
|OVA Logistic Regression|               -                |  19.96%  |

The reason for such less accuracy is because the dataset contains around 800k rows and ML algorithm work well only till 100k. A strong proof for this can be seen with the shoot of accuracy to 83.97% by reducing the dataset to 20% after randomly shuffing it. So we need to use Neural Network approach.
