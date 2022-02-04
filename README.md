# Supervised Machine Learning Challenge: Predicting Credit Risk

## Details About the Challenge
This assignment was designed to challenge me to build a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not.

## Preprocessing: Convert Categorical Data to Numeric
1. Download data from LendingClub and create two CSVs using the [GenerateData Jupyter Notebook](/Generator/GenerateData.ipynb)
   - [2019 Loans CSV](/2019loans.csv)
   - [2020 Q1 Loans CSV](/2020Q1loans.csv)

2. Create a training set from the 2019 loans and convert categorical data to numeric.
   - ![image](https://user-images.githubusercontent.com/88349512/152570530-f3063fe0-a55e-4554-8983-2eed0c080c41.png)

3. Create a testing set from the 2020 Q1 loans and convert categorical data to numeric.
   - ![image](https://user-images.githubusercontent.com/88349512/152570660-d11634c7-c80a-4275-94ec-0aa39b00b7a7.png)

### Predict Which Model Will Perform Better
- I think that the random forest classifier model will perform better here because the data is more categorical.

## Fit LogisticRegression and RandomForestClassifier Models
1. Create a LogisticRegression model, fit it to the data, and print the score.
   - ![image](https://user-images.githubusercontent.com/88349512/152571103-9ae2aabc-b0d4-4cbf-b4a2-0ec00b07503a.png)
   - ![image](https://user-images.githubusercontent.com/88349512/152571977-b5e9e6c2-e676-4b91-b98a-22f9c045bf50.png)

2. Create a RandomForestClassifier model, fit it to the data, and print the score.
   - ![image](https://user-images.githubusercontent.com/88349512/152572019-9a293d0d-0464-4731-918b-ea6b9745240e.png)

## Revisit the Preprocessing: Scale the Data
1. Use StandardScaler to scale the training and testing sets
   - ![image](https://user-images.githubusercontent.com/88349512/152571573-a88cbbd2-971e-4157-a306-35e011b84163.png)

### Predict Which Model Will Perform Better
- I think that the logistic regression model will perform better here because the data has now been scaled and is more numeric than categorical.

### Fit LogisticRegression and RandomForestClassifier Models with Scaled Data
1. Create a LogisticRegression model, fit it to the scaled data, and print the score.
   - ![image](https://user-images.githubusercontent.com/88349512/152572118-70c96f4b-6c67-4934-b18a-112baa70afb0.png)
   - ![image](https://user-images.githubusercontent.com/88349512/152572172-d1496093-0e03-4a04-8dad-ab85efaa1171.png)

2. Create a RandomForestClassifier model, fit it to the scaled data, and print the score.
   - ![image](https://user-images.githubusercontent.com/88349512/152572278-78e0ebe6-486a-4f19-9724-fa3078072285.png)

### Evaluation
How do the model scores compare to each other, and to the previous results on unscaled data?
- Logistic Regression model:
  - Unscaled: 0.5082943428328371
  - Scaled: 0.7598894087622289
  - The scaled data improved greatly with the logistic regression model which means that the attributes that weren't scaled had a bigger impact in this model.
- Random Forest Classifier model:
  - Unscaled: 0.648660144619311
  - Scaled: 0.6329221607826457
  - The data stayed about the same with the random forest classifier model which means that the attributes are not as affected by scaling as they are in the logistic regression model.

How does this compare to your prediction?
- This is in line with my prediction based on the data type: categorical vs. numeric prior to and after the StandardScaler was implemented.

### Run the Code
1. Open and run the [Credit Risk Evaluator Jupyter Notebook](/Generator/Credit_Risk_Evaluator.ipynb) to see the above.
