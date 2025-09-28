# Final-project-Stroke-prediction-data
## Introduction about stroke
Stroke is a major public health problem worldwide and a leading cause of disability and mortality. According to the World Health Organization, a stroke occurs when the blood flow to the area of the brain is interrupted or reduced, causing brain cells to be deprived of oxygen and nutrients. If not treated promptly, this can lead to permanent neurological damage or death.

In this project, I use the Stroke Prediction Dataset available on Kaggle (Fedesoriano et al.) to conduct a data-driven investigation of stroke risk factors. The dataset includes demographic, behavioral, and medical features such as age, gender, hypertension, heart disease, smoking status, body mass index (BMI), and others. 
kaggle.com

My focus is on predicting the likelihood of stroke specifically in males. By narrowing the analysis to the male subset of the data, I aim to identify risk factors and patterns that are particularly relevant for men. Through exploratory data analysis, feature engineering, and machine learning modeling, this study attempts to answer questions such as:

Which variables most strongly influence stroke risk in men?

How accurate can a predictive model be in distinguishing high-risk versus low-risk male patients?

Are there actionable insights or preventive recommendations we can infer for male populations?

The outcomes of this work could contribute to better understanding of gender-specific stroke risk and may guide targeted interventions or awareness programs for men.

## Process in Pyhton
Prediction regression in google colab
### 1. Import neccessary libraries and database by python
At this step, I apply pandas, seabornm, matplotlib, numpy to extract data from kaggle. My database is Stroke prediction database in csv file

The Stroke database: 

<img width="1670" height="310" alt="image" src="https://github.com/user-attachments/assets/e36a585b-8440-4c8c-8c7e-702fc2d407c2" />

<img width="1222" height="942" alt="image" src="https://github.com/user-attachments/assets/e1b1fb6a-e8f7-4241-b7fe-9c23dd6f3e03" />

As we can see, in Bmi column, it has null value and we need to fill it to make the database be useful. The null value need to replace by mean value because it can keep the size of database and mean value is the central tendency value so that the database can be accurately.

<img width="290" height="662" alt="image" src="https://github.com/user-attachments/assets/334920be-db90-48ca-8a1f-5b629007083f" />

After that, I create some EDA univariable and bivariate to check the distribution of data

<img width="1549" height="1476" alt="image" src="https://github.com/user-attachments/assets/ca241327-0702-4a64-bcea-af7ed7808eea" />

<img width="1614" height="1783" alt="image" src="https://github.com/user-attachments/assets/a09813be-1583-4092-bec2-272703975380" />

In this database, I want to focus mainly on 3 columns: Age, Bmi and Avg_glucose_lvel because there are 3 main factors can lead to stroke and they need to be analyzed to research and reduce their impact.
