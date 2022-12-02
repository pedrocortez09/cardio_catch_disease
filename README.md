# <p align="center" dir="auto">Cardio Catch Disease</p>
## <p align="center" dir="auto">Predictiong Cardiovascular Disease</p>
<div align="center">
<img src="https://user-images.githubusercontent.com/103151311/205302658-a4d71859-6eba-422f-80d0-1284379540db.png" width="700" />
</div>

# 1. Business Problem.

Cardio Catch Diseases is a company specialized in detecting heart disease in the early stages. Its business model lies in offering an early diagnosis of cardiovascular disease for a certain price. </p>
Currently, the diagnosis of cardiovascular disease is manually made by a team of specialists. The current accuracy of the diagnosis varies between 55% and 65%, due to the complexity of the diagnosis and also the fatigue of the team who take turns to minimize the risks. The cost of each diagnosis, including the devices and the payroll of the analysts, is around $1,000.00. </p>
The price of the diagnosis, paid by the client, varies according to the precision achieved by the team of specialists.


Exam Accuracy   | Price | Rules | Example
:---------  | :------ | :------ |:---------
Above 50%   | min $500.00 | +$500 for each additional 5% precision | Precision = 60% -> $1,000.00
Up to 50%   | $0.00  | N/A | N/A |


Thus, we see that different values in the exam precision, given by the team of specialists, make the company either have a profitable operation, revenue greater than the cost, or an operation with a loss, revenue less than the cost. This instability of the diagnosis makes the company to have an unpredictable cashflow.


# 2. Business Assumptions.

The assumptions about the business problem is as follows:

- CVDs are the number 1 cause of death globally: more people die annually from CVDs than from any other cause.
- An estimated 17.9 million people died from CVDs in 2016, representing 31% of all global deaths. Of these deaths, 85% are due to heart attack and stroke.
- Over three quarters of CVD deaths take place in low- and middle-income countries.
- Out of the 17 million premature deaths (under the age of 70) due to noncommunicable diseases in 2015, 82% are in low- and middle-income countries, and 37% are caused by CVDs.
- Most cardiovascular diseases can be prevented by addressing behavioural risk factors such as tobacco use, unhealthy diet and obesity, physical inactivity and harmful use of alcohol using population-wide strategies.
- People with cardiovascular disease or who are at high cardiovascular risk (due to the presence of one or more risk factors such as hypertension, diabetes, hyperlipidaemia or already established disease) need early detection and management using counselling and medicines, as appropriate.


# 3. Solution Strategy

My strategy to solve this challenge was:


**Step 01. Data Description:** My goal is to use statistics metrics to identify data outside the scope of business.

**Step 02. Feature Engineering:** Derive new attributes based on the original variables to better describe the phenomenon that will be modeled.

**Step 03. Data Filtering:** Filter rows and select columns that do not contain information for modeling or that do not match the scope of the business.

**Step 04. Exploratory Data Analysis:** Explore the data to find insights and better understand the impact of variables on model learning.

**Step 05. Data Preparation:** Prepare the data so that the Machine Learning models can learn the specific behavior.

**Step 06. Feature Selection:** Selection of the most significant attributes for training the model.

**Step 07. Machine Learning Modelling:** Machine Learning model training

**Step 08. Hyperparameter Fine Tunning:** Choose the best values for each of the parameters of the model selected from the previous step.

**Step 09. Convert Model Performance to Business Values:** Convert the performance of the Machine Learning model into a business result.

**Step 10. Deploy Modelo to Production:** Publish the model in a cloud environment so that other people or services can use the results to improve the business decision.

# 4. Top 3 Data Insights

**Hypothesis 01:** People with a high BMI tend to have heart problems.

**True** - The higher the person's BMI, the more likely they are to have a cardio disease.


**Hypothesis 02:** 50% of people who smoke have a cardio disease.

**False.** - It's False, but the percentage is 46,59% which is almost half of the people


**Hypothesis 03:** 80% of people who practice physical activity do not have cardio disease. 

**False.** - Only 51.33% of people who exercise do not have cardio disease.

# 5. Machine Learning Model Applied

Tests were made using different algorithms.

# 6. Machine Learning Modelo Performance

The chosen algorithm was the **LGBM Classifier**.

## Precision, Recall, ROC AUC and other metrics

These are the metrics obtained from the test set.

Precision   | Recall | F1 Score | ROC AUC | Accuracy
:---------  |:------|:------ |:--------- |:------
0.741       | 0.703  | 0.721   | 0.796 | 0.730  

# 7. Business Results

Let's recap the pricing model. The price of the diagnosis, paid by the client, varies according to the precision achieved by the team of specialists.

Exam Accuracy   | Price | Rules | Example
:---------  | :------ | :------ |:---------
Above 50%   | min $500.00 | +$500 for each additional 5% precision | Precision = 60% -> $1,000.00
Up to 50%   | $0.00  | N/A | N/A |

Our full dataset has 70.000 clients. Assuming that all clients in the database went to the clinic to make a diagnosis, using our model which has an accuracy ranging from 72% - 76%, the value of all diagnoses compared to the current model would be:

Models |	Best |	Worst
:-------|:-----|:-------
Our Model |	$183,400,000.00 |	$154,000,000.00
Current |	$105,000,000.00 |	$35,000,000.00

# 8. Conclusions

- Our model guarantees an accuracy of around 75%, which means a best case profit of $148,400,000.00

# 9. Lessons Learned

- It's very important to understand every metric to chose the best one according to the business problem.

# 10. Next Steps to Improve

1. **Develop an app** that intakes a portfolio of patients and assigns for each patient its respective probability of presenting a cardiovascular disease.
2. **Run a Design Discovery** to uncover facts that could be missing in our analysis in order to enrich the data that we have and improve the model performance.
3. **Build a model retraining pipeline**.

