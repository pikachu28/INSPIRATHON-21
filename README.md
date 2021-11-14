# INSPIRATHON-Team Captain Denver

## Problem Statement:

You need to come up with a solution to protect women globally from social media harassment. Develop a product where online trolling and harassment can be controlled as well as there is a feature to collect information about trollers and report them accordingly. Your tool should be able to identify bots and trolls. You can also add a feature to carry out historical analysis and predictive analysis based on existing tweets or posts to identify potential trollers and report them if needed. The system should also ensure data privacy and implement complete anonymity if and when required.

## Proposed Solution:

-Increasing use of internet has lead to increase in the cyberbullying.

-Using ML Models to classify the sentiments of the comments made on women as offensive and non-offensive.

-Considering **Twitter** as one of the platform where various kinds of trolls occur everyday. We use **Twitter APIs** to scrap post based on the keywords to test our model.

-Using **Chrome Extension** to block accounts who troll frequently.


### Tech stack:

Python, Natural Language Processing, StreamLit

Various Tools like Numpy, pandas, matplotlib, tweepy

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

**Best Performed Model: **Stochastic Gradient Descent
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


  
 Build & Designed _Dynamic Dashboard_ using **Streamlit** for Data Visualisation in training and testing data and deploy the **Stochastic Gradient Descent Model** and.

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




https://user-images.githubusercontent.com/62153950/141665440-0293dfb3-8898-4c49-963f-bd87df4b76ba.mov

## Block Trolls : A chrome extension in building phase
Twitter has become a breeding grounds sociopaths, conservatives who try to impose their belives by polluting your tweets or feeds. As a person with many followers it become difficult to block everyone of them so here are we to optimize your task and save your time and mental piece, all you have to so is just add this chrome extension and imagine a clean and positive twitter feed coming your way.

The logic to how users will be blocked can be found in the js files,we have used jQuery for extracting the information.

Deploying this chrome extension in order to provide a full time analysis to real time twitter using people comes to our future scope as we believe in optimizing our coding standards before realising the beta version.
_This chrome extension can automatically block accounts with_

```
Default profile pictures
Screen names ending with 8 digits
No profile text
Fewer than a certain number of followers
Certain keywords in their profile
Certain keywords in their user name
All of these can be configured to your taste. Only the first two are enabled by default.
```

This does not block accounts who you follow simply **tweet keywords**. The extension scans the page for tweets, evaluates the username and profile picture. If those are fine, it fetches their profile and looks for the keywords. If a block is warranted, it triggers the click events for the block button and the block confirmation dialog. If a user is cleared, it'll skip checking them going forward until the page is reloaded.

## Future Scope

1. Report the posts that are offensive.
2. Blocking the posts to be uploaded whose sentiments have offensive meaning against women on social media platforms.
3. Deploying the Chrome Extension to block frequently accounts.


