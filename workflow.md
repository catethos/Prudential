General Data Science Workflow
==============================

![](images/process.png)

1. Defining the problem
  - What decisions are the client trying to make
  - How to measure the quality of the decision
  - What are the uncertainties in the decision making process
  - What extra information is needed to make the decisions
  - What is the cost of reducing the uncertainty
  - What is the value of additional information
2. Collecting the data
  - What is the data neneded
  - Estimate the value of the data so that we can collect the most valuable data first.
  - Design the data collection pipeline
  - Ensure the quality of data collected
3. Cleaning and transforming the data
  - Transform the data into a suitable format for analysis
  - Ensure the data processing is reproducible.
4. Analysing and modeling the data
  - Exploratory Data Analysis (EDA)
    - Descriptive analysis of the data
    - Looking for big pattern
    - Checking if there is any error in the data collection process
  - Establishing baseline
    - Build the simplest model, for example, multiple regression
    - The model should be easy to understood and act as a sense checking device when developing more sophisticated models
  - Model building
    - Improving the baseline model by employing more sophisticated machine learning algorithms and statistical models, for example deep learning and hierachical models.
    - Using cross-validation to ensure the model can generalize to unseen data.
    - Choosing the best model or use ensemble of different models
5. Comminicating the result
  - Report generation
  - Dashboard visualisation
  - Deployment as a service for the consumption of different business unit.


Data Collection
===============
![](images/data.png)

We are trying to collect two types of data:
1. **Prediction** the values we are trying to predict that can affect the decison making process. For example, job performance and attrition rate. This type of data consists of any values/measurements/records that constitute the values we want to predict.

2. **Predictors** the values that we think are important in predicting. It reflects our holistic view about human nature for it consists of
  - hard traits such as experience, demography, and social economy status.
  - soft traits such as everything inside our PICA framework

Predictor
---------

| Data Group | Data                      | Paper  | Collection Method  |
| ---------- | ------------------------- | ------ | ------------------ |
| Experience | Previous Jobs             |        |                    |
| Experience | New joiner/rejoin         |        |                    |
| Experience | Tenure                    |        |                    |
| Education  | Level                     |        |                    |
| Education  | Major                     |        |                    |
| Education  | University/High School    |        |                    |
| PICA       | Self-reported Personality |        | Assessment         |
| PICA       | Social media Personality  | [1][1] | Fb/Twitter account |
| PICA       | Vocational Interest       | [2][2] |                    |
| PICA       | Culture                   |        |                    |
| PICA       | Cognitive Ability         | [3][3] |                    |
| Demography | Gender                    | [4][4] |                    |
| Demography | Marital Status when join  |        |                    |
| Demography | Current Marital status    |        |                    |
| Demography | Parental Education        | [5][5] |                    |
| Demography | Parental Occupations      | [5][5] |                    |

*Note*: Demography data can be used to predict cognitive ability https://homepages.abdn.ac.uk/j.crawford/pages/dept/pdfs/BJCP_1989_Demographic_Premorbid_IQ.pdf

[1]: https://www.sciencedirect.com/science/article/pii/S0191886917307328
[2]: https://www.jstor.org/stable/41613576
[3]: https://www.ncbi.nlm.nih.gov/pubmed/14717634
[4]: https://www.sciencedirect.com/science/article/pii/S0191886917307328
[5]: https://opensiuc.lib.siu.edu/cgi/viewcontent.cgi?article=2276&context=theses


Prediction
----------

| Data                | Paper | Collection Method |
| ------------------- | ----- | ----------------- |
| Sales               |       |                   |
| Number of customers |       |                   |
| Managers            |       |                   |
| Peer reviews        |       |                   |
| Job Satisfaction    |       |                   |


Notes
=====
![](images/big5.jpg)
