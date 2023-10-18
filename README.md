# Project Name: ML_Classification_DecisionTree_Analysis
Consider the 'drug200.csv' file. It has a column named 'Drug'. It is the classification class in the data set. Using the feature set, I develop decision tree to easily classify the unknown or a future item in its class. Classification is a Supervised Machine Learning model that help to classify an unknown or future item by observing similarity. Now, KNN is also used for this purpose. But using decision tree reduces the length of KNN process as it does not require multiple test to determine best model.

## Supervised Machine Learning Model

The term 'Supervise' means to observe and direct the execution of a task, project or activity. In this type of Machine Learning the Client( The coder or data Scientist) supervise the model by teaching so that it can predict unknown or future instances. We teach the model by using training data. One thing to remember that the training data must be labeled. In this case, column names are called attributes, columns are called features.

## Classification Process

A supervised Machine Learning algorithm, used to categorize some unknown items into a discete set of categories or classes. It uses the characteristics of the unknown item. For example, suppose a data set that consider whether a tumor cell in human body is bening or malignent. After observing say 100 data points, we train a model and using that we are prediting the next tumor will be bening or malignent depending on the features the tumor will have.

## Decision Tree Algorithm

Narendra Nath Joshi said "The basic intution behind a decision tree is to map out all possible decision paths in the form of a tree". A decision tree is a tree like structure that helps to classify an unknown item or future data. These are made by splitting the training set into different nodes. Now, which attribute is the first node to distribute is determined by the entropy of the node. Our goal is to select the node that increases the purity of the step. In general, decision trees are amde of Nodes and branches. The term **Entropy** measures the uncertainty and randomnes in the step or node.

## About the 'drug200.csv' data set

Here we cosider the drug200.csv data. It is available in GitHub and Kaggle. The data set has 200 observations and 6 columns/variables. Among these 6 columns. These 6 columns are **Sex**, **Age**, **BP**, **Cholesterol**, **Na_to_K** and **Drug**. Among these columns we consider the first 5 columns as feature sets. In the feature set, **Sex**, **BP**, **Cholesterol** are categorical in nature. The column **Drug** is considered as the target variable.

## Project Steps

**1. Basic Data Exploration:**

It is the first step of any project. In this step, I read the data set using pandas read_csv() function and save the result in a variable called df. I also check the first five observations along with the column names. I check the dimension of the data set, the column names of the data set and also check the column types of the data set.

**2. Defining Feature set and Target Variable:**

In the second step, I define the feature set denited by **x** and the target set denited by **y**. The feature set is the data frame that contains the values for the **Sex**, **Age**, **BP**, **Cholesterol** and **Na_to_K** columns. As sklearn works only on array types data, I convert them to array by using .values method. Similarly, the **Drug** column is working as target cariable.

**3. Categoricaal to Numerical Conversion:**

sklearn's decision tree modules (DecisionTreeClassifier) doesn't work on categorical type data sets. In order to work it out properly, I convert them into numerical values using **LabelEncoder() object of preprocessing module of sklearn** package. Using this object, it is very easy to convert them into numerical value. The first mentioned category is replaced by 0, the next mentioned category is replaced by 1 and so on.

**4. Train Test Data Split:**

To build the model, it is necessary to break the model into two parts, they are Training set (the set used to build the model) and the test part (used to check model accuracy). Here 70% of the total data set ( 70% of 200 observations) are considered as training set and the rest is considered as test data set. By using the **model_selection module of sklearn** library, we can easily split the data set. By using this method, we get four different data sets for diffferent purposes. The model is build by using the train_x and train_y set. The predicted values are obtained using the test_x data seT. Finally, to compare the predicted values with actual response of test set, y_test data set is used. I also check the dimensions of the four sets so that the split is proper and it reflects exactly, what I needed.

**5. Model Building, Prediction and Decison Tree Accuracy:**

In this step, I build the model using train_x and train_y data set. To build the model, I use DecisionTreeClassifier function and select **Entropy** as my required criteria. This criteria is set to **entropy** means that I am building the decision tree by splitting the model with the attribute that has lowest entropy. After prediction, I get the predicted values and also get the actual response values. By observing first 10 values, I understand that the result i get is very much same as the actual response value. This statement is also supported by the Decision Tree acuuracy (which is approximatly 98%) calculated by using the **metrics module of sklearn** library.

**6. Getting the Decision Tree:**

In the final step of the project, I plot the decision tree using the **tree module of sklearn and the matplotlib** library. The diagram is added in the file Section.

** THIS COMPLETES THE PROJECT ON CLASSIFICATION USING DECISION TREE**












