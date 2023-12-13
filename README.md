# Terror Attacks in Europe

## Introduction

Predicting casualties in a terror attack is a complex and challenging task that involves the analysis of various factors, including the type of attack, target location, and the nature of the weapon used. Machine learning models and statistical analyses can be employed to assess historical data, patterns, and trends to identify potential risk factors and develop predictive models. However, due to the dynamic and unpredictable nature of terrorism, achieving precise predictions is inherently difficult. Ultimately, while predictive tools can contribute to risk assessment, comprehensive counter-terrorism strategies should encompass a multi-faceted approach involving intelligence, international cooperation, and community engagement to enhance overall preparedness and response capabilities.

## Data

The Global Terrorism Database (GTD) is an open-source database including information on terrorist attacks around the world from 1970 through 2017. The GTD includes systematic data on domestic as well as international terrorist incidents that have occurred during this time period and now includes more than 180,000 attacks. The database is maintained by researchers at the National Consortium for the Study of Terrorism and Responses to Terrorism (START), headquartered at the University of Maryland. Our focus in the project is to predict if there will be any casualties in terror attacks in Europe.

## Libraries Used

Following Libraries are used in this project

- numpy: for mathmatical operations
- pandas: for handling tabular data
- openpyxl: for reading the excel data file
- matplotlib: for visualization
- seaborn: for visualization
- plotly: for visualization map
- kaleido: for visualization renderer
- scikit-learn: for ML models

Install the above libraries using `requirements.txt` and following command

```sh
foo@bar:~$ pip install -r requirements.txt
```

## Files

The project contains two files.

- `globalterrorismdb_0522dist.xlsx`: Dataset in excel format downloaded from [Kaggle](https://www.kaggle.com/datasets/START-UMD/gtd).
- `Project.ipynb`: A Python-based Jupyter notebook that encompasses all of our analyses.

## Results

We constructed and fine-tuned various classification models to predict whether a terrorist attack leads to any casualties using following feature

- Type of Attack, Weapon, Target
- Month & Country of the Attack
- Number of hostages
- Success/Failure of the Attack

Here are the results based on some Accuracy and ROC-AUC metrics
| Model | Accuracy | ROC-AUC |
| :-----------------------: | :------------: | :-----------: |
| Decision Tree | 0.784 | 0.769 |
| Logistic Regression Tuned | 0.752 | 0.801 |
| Logistic Regression | 0.753 | 0.801 |
| Random Forest | 0.772 | 0.812 |
| Decision Tree Tuned | 0.796 | 0.821 |
| Gradient Boosting | 0.799 | 0.835 |
| Gradeint Boosting Tuned | 0.803 | 0.841 |
| Random Forest Tuned | 0.807 | 0.848 |

Following fine-tuning, the Random Forest model demonstrated superior performance, achieving the highest ROC-AUC score of 0.85.
