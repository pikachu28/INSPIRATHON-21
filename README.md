# INSPIRATHON

## Problem Statement:

You need to come up with a solution to protect women globally from social media harassment. Develop a product where online trolling and harassment can be controlled as well as there is a feature to collect information about trollers and report them accordingly. Your tool should be able to identify bots and trolls. You can also add a feature to carry out historical analysis and predictive analysis based on existing tweets or posts to identify potential trollers and report them if needed. The system should also ensure data privacy and implement complete anonymity if and when required.

## Proposed Solution:

-Increasing use of internet has lead to increase in the cyberbullying.

-Using ML Models to classify the sentiments of the comments made on women as offensive and non-offensive.

-Considering Twitter as one of the platform where various kinds of trolls occur everyday.

-So, Twitter APIs to scrap post based on the keywords to test our model.


### Tech stack:

Python, Natural Language Processing, StreamLit

Various Tools like Numpy, pandas, matplotlib

## Features 

### Detect of Trolls on Social Media

#### Training Data Visualization

<img width="1433" alt="Screenshot 2021-11-14 at 7 40 20 AM" src="https://user-images.githubusercontent.com/62153950/141664724-2e53a245-8fb4-44d1-9fd7-182d08273cbe.png">
<img width="1440" alt="Screenshot 2021-11-14 at 7 40 59 AM" src="https://user-images.githubusercontent.com/62153950/141664735-02a8a819-b932-422e-b9db-d5716ede226d.png">
<img width="1438" alt="Screenshot 2021-11-14 at 7 44 19 AM" src="https://user-images.githubusercontent.com/62153950/141664785-24dc2383-e5da-4057-963e-09f81a507ee4.png">
<img width="1440" alt="Screenshot 2021-11-14 at 7 44 04 AM" src="https://user-images.githubusercontent.com/62153950/141664791-2bf3da6a-d157-4558-a5c2-ea29aaf30cc5.png">



#### Training


Training various Baseline Machine Learning model like Stochastic Gradient Descent, KNN, AdaBoostClassifier, MultinomialNB etc. for classification of tweets between offensive and non-offensive towards females.

Various ML Model Analysis :
<img width="1015" alt="Screenshot 2021-11-14 at 7 23 14 AM" src="https://user-images.githubusercontent.com/62153950/141664468-8d2db05d-54e5-4545-a3f2-ad4a150135d4.png">

Time Complexities:
<img width="1022" alt="Screenshot 2021-11-14 at 7 25 57 AM" src="https://user-images.githubusercontent.com/62153950/141664486-f1dbe0f9-5625-42e6-ba0a-4f311dc5a685.png">

Conclusion: The Algorithms Bagging, SGD, Logistic Regression and Decision Tree and Random Forest and LinearSVC have more or less similar performance. We will tune the hyperparameters of these algorithms. However, the training time for Bagging is very high as compared to the others. Hence we drop it. 

Hypertuning the Parameters gives:

Best Performed Model: Stochastic Gradient Descent
```
SGDClassifier

Optimized Model
------
Best Parameters: {'alpha': 0.0002, 'max_iter': 3000}
Accuracy: 0.9270
F1-score: 0.9431
Precision: 0.9669
Recall: 0.9204
```

#### Testing

Using Twitter APIs to scrap 10 post and classify them between offensive and non-offensive.

<img width="1440" alt="Screenshot 2021-11-14 at 7 42 11 AM" src="https://user-images.githubusercontent.com/62153950/141664756-a6012d91-6f8e-4136-938d-8fec71e05ca4.png">

 
 #### Testing Data Visualization
 
<img width="1440" alt="Screenshot 2021-11-14 at 7 43 00 AM" src="https://user-images.githubusercontent.com/62153950/141664771-ecb79a80-9c31-4e4c-8be4-4aa06fbcf5f9.png">


  
 Build & Designed Dashboard using streamlit for Data Visualisation in training and testing data and deploy the Stochastic Gradient Descent Model and.

### Run On Local System

Clone the Repository:

```
git clone https://github.com/pikachu28/INSPIRATHON.git
```
cd into Detect_trolls folder via root path

```
cd myProject_rootPath/Detect_trolls
```

Create the Virtual Environment
```
virtualenv my_name
```
Dashboard is build on Python 3.7.

Activate the Environment 
```
source virtualenv_name/bin/activate
```
Install the requirements
```
pip install -r requirements
```
Run the streamlit file
```
streamlit run app.py
```
#### Dashboard will open at http://localhost:8501/ 

#### Home View Would be:
<img width="1438" alt="Screenshot 2021-11-14 at 7 56 03 AM" src="https://user-images.githubusercontent.com/62153950/141665003-289c5e40-67ca-424a-97c5-7d1a2d724da2.png">




