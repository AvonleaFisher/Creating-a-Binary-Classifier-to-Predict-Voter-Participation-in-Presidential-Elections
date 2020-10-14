# Creating a Binary Classifier to Predict Voter Participation in Presidential Elections

## Introduction 
The aim of this project is to build a binary classification model for predicting whether an eligible voter did not vote in the 2016 presidential election, using  a selection of data from the 2018 General Social Survey. The General Social Survey collects demographic, behavioral, and attitudinal data on a large and diverse sample of US respondents. The dataset used in this project was created by selecting variables from the survey using the GSS Data Explorer and can be accessed [here](https://gssdataexplorer.norc.org/projects/86577/extracts). Note: you must create a GSS Data Explorer account to download the data.

Past research has suggested that socioeconomic variables such as education, wealth, and occupation are strong predictors of voter turnout. Features in this subset include a variety of socioeconomic variables, as well as variables related to respondents' political attitudes. 

The ability to predict if an eligible voter did not vote can be used to increase overall voter turnout in future elections. It is important to note that any model designed to predict human behavior is inherently limited, in that an individual's attitudes, motivations and circumstances can change within a given period of time—and especially over the course of an entire preseidential term. Furthermore, there is a diversity of views about the value and efficacy of voting, and some eligible voters may abstatin from it on principle. This project does not assume that every non-voter can or should choose to vote, but is intented to serve only as a guideline for voter engagement organizations that are interested in focusing on likely non-voters.

## Methods
After exploring, cleaning, and numerically encoding the data, several binary classifiers were built and then optimized with scikit-learn. Logistic regression, random forest, and gradient boosting classifiers were compared. Due to class imbalance, accuracy scores were given limited consideration in the evaluation of model performance. The best-performing model was instead chosen based on recall in order to maximize the number of correctly identified non-voters.

## Results
The random forest model had the best recall score and overall performance:


<b>Recall:</b> .73
<br>
<b>Precision:</b> .78
<br>
<b>F1:</b> .75
<br>
<b>AUC:</b> .84
<br>
<b>Accuracy:</b> .89

## Recommendations 
Respondents' participation in the 2012 election was the strongest predictor of voting in the 2016 election, which suggests that past voting behavior may predict an eligible voter's participation in future elections. Political identity was also a strong predictor: respondents who think of themselves as extremely conservative or extremely liberal were more likely to have voted in 2016 than political moderates. Voter turnout rates also appeared to be positively linearly related to age.

With these observations in mind, organizations seeking to increase voter turnout by engaging potential non-voters should prioritize those who haven't voted in past elections, younger voters, and political moderates.

## Limitations and Next Steps
Many features were transformed and or excluded from the original dataset to foster a simpler and more legible encoding process. Future analysis should attempt to find or collect more complete data with similar variables. Additionally, models can be further optimized through an exhaustive grid search.
