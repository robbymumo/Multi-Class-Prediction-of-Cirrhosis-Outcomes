# MULTI-CLASS PREDICTION OF LIVER CIRRHOSIS OUTCOMES.

## PROJECT BY:

* Robinson Musau.
* Kelvin Rotich.

## INTRODUCTION

Welcome to this project on predicting liver cirrhosis outcomes on different patients. In this project we will focus on supervised learning algorithms and choose the best one based on the log-loss metric. This is based on a comprehensive dataset that contains different factors about patients that may or may not lead to one of the outcomes from the disease. 

The main purpose of this project is to create a predictive model that accurately classifies the outcome of a patient after medication. This project aims to provide insights to the medical practicioners and in turn they may be able to get positive outcomes after treating their patients.

In the following sections we will delve into the project's methodology, key findings and the models' performance in predicting liver cirrhosis.

## PROJECT OVERVIEW.

### Liver cirrhosis background.

Liver cirrhosis involves progressive scarring of the liver, often caused by factors like chronic alcohol abuse, viral hepatitis, or fatty liver disease. Treatment strategies vary based on the underlying cause. Lifestyle changes, such as alcohol cessation or weight management are crucial. Medications may be prescribed to manage symptoms and address specific causes. In advanced cases, liver transplants might be considered as a viable option. Regular medication monitoring and adherence to prescribed treatments are essential for managing liver cirrhosis effectively.

### Challenges caused by liver cirrhosis.

Liver cirrhosis posses various challenges due to its impact on liver function. Patients often experience complications like ascites, which is the fluid buildup in the abdomen, brain dysfunction and increased vulnerability to infections. The compromised liver function affects blood clotting, leading to easy bruising and bleeding. Malnutrition can also occur as the liver stuggles to process nutrients, contributing to muscle wasting and weakness. Additionally, cirrhosis increases the risk of liver cancer. 

### Solutions to mitigate liver cirrhosis.

Mitigating liver cirrhosis involves addressing underlying causes and managing complications. Lifestyle changes play a major role, including alcohol abstinence for those with alcohol cirrhosis and adopting a healthy diet to manage non-alcoholic fatty liver disease. Antiviral medication can help control viral hepatitis, and weight managememt is vital for those with obesity-related liver disease. Medications may be prescribed to manage symptoms and complications. In some cases, liver transplants become a viable option for viable cirrhosis. Regular medical check-ups, vaccination against hepatitis and early intervention are key components of a comprehensive strategy to mitigate liver cirrhosis.

### Problem statement.

The challenge of predicting liver cirrhosis outcomes involve developing a robust predictive model capable of accurately categorizing patients into their outcomes of the disease. This task requires addressing challenges such as the diverse etiology of cirrhosis, varying progression rates and presence of multiple complications. Achieving accurate predictions neccesitates comprehensive data integration, considering clinical, laboratory and imaging variables. Additionally, the model should account for the dynamic measure of cirrhosis and potential shifts in patient status over time. The developement of an effective predicting system for liver cirrhosis outcomes is crucial for personalized treatment strategies and timely interventions to improve patient outcomes.

## DATA UNDERSTANDING.

The two datasets used for this project were acquired from `Kaggle.com`.From the training dataset, we can see that we have a dataset with 7905 rows and 20 columns. The test dataset has 5271 rows and 19 columns. The one column missing is the `Status` column which will be determined by the model we create. 

Additional column information:

* `id`: Patient id.
* `N_days`: Number of days the patient is on treatment.
* `Drug`: Type of drug the patient used for treatment.
* `Age`: Age of the patient in days.
* `Sex`: Gender of the patient.
* `Ascites`: If the patient has ascites(the condition in which fluids collect in spaces within their abdomen) or not.
* `Hepatomegaly`: If the patient has hepatomegaly(their liver is enlarged beyond normal size) or not.
* `Spiders`: If the patient has spider nevi(a common sign of liver disease) or not.
* `Edema`: If the patient has edema(a swollen liver) or not.
* `Bilirubin`: Levels of bilirubin(yellowish pigment made during the breakdown of red blood cells) in the patient's body.
* `Cholesterol`: Levels of cholesterol in the patient's body.
* `Albumin`: Levels of albumin(a protein made by the liver) in the patient's body.
* `Copper`: Levels of copper in the patient's body.
* `Alk_phos`: Levels of alkaline phosphate in the patient's body.
* `SGOT`: SGOT medical test scores. This was used to determine whether the liver was damaged.
* `Tryglicerides`: Levels of truglicerides(a type of fat in the blood) in the patient's body.
* `Platelets`: Levels of platelets in the patient's body.
* `Prothrombin`: Levels of prothrombin(A protein made by the liver) in the patient's body.
* `Stage`: The cirrhosis stage the patient is in.
* `Status`: is the categorical target; `C` (censored) indicates the patient was alive at `N_Days`, `CL` indicates the patient was alive at `N_Days` due to a liver transplant, and `D` indicates the patient was deceased at `N_Days`. 




