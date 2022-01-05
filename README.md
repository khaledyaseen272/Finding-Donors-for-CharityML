# Project: Finding Donors for CharityML
## by: Khaled Yaseen

## Project Overview
In this project, I will apply supervised learning techniques and an analytical mind on data collected for the U.S. census to help CharityML (a fictitious charity organization) identify people most likely to donate to their cause. I will first explore the data to learn how the census data is recorded. Next, I will apply a series of transformations and preprocessing techniques to manipulate the data into a workable format. 
I will then evaluate several supervised learners on data, and will decide which is best suited for the solution from my point of view. Afterwards, I will optimize the model I've selected and present it as a solution to CharityML. Finally, I will explore the chosen model and its predictions under the hood, to see just how well it's performing when considering the data it's given.

## Project Highlights
It is my first project on machine learning. I got acquainted with the many supervised learning algorithms available in sklearn, I had to shortlist 3 or 4 algorithms to evaluate according to the data characteristics and evaluation methods then decided which is the best suitable model. once I chose the suitable algorithm which was 'AdaBoostClassifier', I used grid chearch to tune the model. 

## Target Label And Features
The main target is to predict individuals who make more than, or at most, $50,000 annually with the assumption that individuals who make more than $50,000 annually have a high probability to donate. The dataset features which I will study to make predictions:

- age.
- workclass: Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked.
- education: Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool.
- education-num.
- marital-status: Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse.
- occupation: Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct,  - Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces.
- relationship: Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried.
- race: Black, White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other.
- sex: Female, Male.
- capital-gain.
- capital-loss.
- hours-per-week.
- native-country: United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands

## Software Used
I used the following software and Python libraries:

- [Python 2.7](https://www.python.org/download/releases/2.7/)
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [matplotlib](http://matplotlib.org/)

## Project files
This project contains three files:

- `finding_donors.ipynb`: This is the main file where you will be performing your work on the project.
- `finding_donors.html`: the main file in HTML format.
- `census.csv`: The project dataset which loaded in the notebook.
- `visuals.py`: A Python file containing visualization code that is run behind-the-scenes.

## Conclusion
From the data characteristics, I decided to study 3 alogirthns to choose from them, I studies: Logistic Regression, Gaussian Naive Bayes, and AdaBoost classifier. After creating a training and predicting pipeline, In terms of the metrics, the two highest models in F-score are the logistic regression and AdaBoost Classifier without huge difference between them including when 100% of the testing set is used and Though the logistic regression has a shorter training time but the logistic regression may loss performance because of its high bias and low variance and that is the Strength of AdaBoost Classifier which has the ability to adjust the bias and variance so I decided to choose the AdaBoost Classifier. After doing the model tuning for the AdaBoost Classifier, It gave me accuracy score: 0.8609 and F-score: 0.7316. Finally, I applied feature_importances method for the model and found the most important features are: education-num, hours-per-week, capital-gain, age, and capital-loss.
