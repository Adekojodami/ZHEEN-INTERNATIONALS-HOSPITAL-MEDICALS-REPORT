# ABSTRACTS

! [](med dash1.png) 

# INTRODUCTION

## Background History

Cardiovascular diseases remain a leading cause of morbidity and mortality worldwide, placing an enormous burden on public health systems. Early detection of risk factors is crucial for reducing preventable deaths. The heart attack datasets were collected at Zheen hospital in Erbil, Iraq. 
Clinical indicators such as heart rate, blood pressure, blood sugar levels, CK-MB, and Troponin are vital in diagnosing and predicting cardiovascular conditions. Modern data analysis tools enable healthcare professionals to discover patterns and risk factors associated with these indicators, enhancing clinical decision-making and patient outcomes.
The research under consideration captures essential patient information, including demographics (age, gender), vital signs (heart rate, blood pressure), and biomarkers (CK-MB, Troponin) alongside test results. Analyzing this dataset provides a valuable opportunity to uncover trends, relationships, and risk factors that can guide targeted interventions and improve patient management.

## Problem Statement

Despite the availability of patient clinical data, it is often underutilized in predicting cardiovascular risk and informing clinical decisions. Without systematic analysis, critical insights that could improve early diagnosis and patient care remain hidden. This research seeks to bridge that gap by analyzing key clinical indicators to:
•	Identify patterns that differentiate between positive and negative test results.
•	Understand the relationship between demographic factors and clinical outcomes.
•	Provide healthcare practitioners with data-driven insights to enhance patient management and outcomes.

## OBJECTIVES
The research aims are to analyze clinical and demographic data to identify key factors influencing test results and outcomes, ultimately supporting predictive modeling and informed clinical decision-making. To identify significant patterns and relationships between indicators (e.g., CK-MB and Troponin) and test results. To evaluate the influence of age, gender, and other demographic factors on patient test results.

 
## DATA DESCRIPTION

-DATA SOURCE: 
The datasets were gotten from Kaggle about records of Zheen hospital in Erbil, Iraq
-Data collection: 
The data was an excel.csv file and was imported into Power BI Desktop.

**Data Characteristics:**
**Description:**
The data consists of table with 1320 rows and 9 columns. The column titles are Age, Gender, Heart Rate, Systolic Blood Pressure, Diastolic Blood Pressure, Blood Sugar, CK-MB, Troponin and Results. However, additions of two columns were created such as gender class and age class.
 








## METHODOLOGY

### Data Cleaning:
Data cleaning was done on the datasets, whereby all the datasets are errors free and its validity is 100%.
To perform data cleaning and preparation of the medical datasets in Power BI Desktop, follow these steps:
1. Import the Dataset
•	Step 1: Open Power BI Desktop
•	Step 2: click on get data from home tab.
•	Step 3: Then click on Text/CSV icon.
•	Step 4: Then import your CSV files dataset.
•	Step 5:  Click on Transform Data.

2. **Data Modelling** 
 


3. **DATA ANALYTICS EXPRESSION (DAX)**
   
I.	Patients Age = sum(Medicaldataset[Age])

II.	Patients Heart Rate = sum(Medicaldataset[Heart rate])

III.	No of Female = CALCULATE(COUNT('Medicaldataset'[Gender]),
    'Medicaldataset'[Gender class] IN {"Female"})
    
IV.	No of Male = CALCULATE(COUNT('Medicaldataset'[Gender]),
    'Medicaldataset'[Gender class] IN {"Male"})
    
V.	Gender class = if(Medicaldataset[Gender]>=1,"Male", if(Medicaldataset[Gender]<=0,"Female"))

VI.	Age class = if(Medicaldataset[Age]>=65,"65+", IF(Medicaldataset[Age]>=45,"45-64", IF(Medicaldataset[Age]>=35,"35-44",IF(Medicaldataset[Age]>=25,"25-34", IF(Medicaldataset[Age]<=25,"14-24")))))





 
## RESEARCH QUESTIONS

1. Are older patients more likely to have a positive result?
   

2. How do CK-MB levels vary between positive and negative outcomes?
 

3. Are there gender differences in test results?
 

4. Does high blood sugar correlate with positive test results?

   
 
5. What’s the relationship between Troponin and CK-MB levels?
 











## RESULTS

Results from Zheen International Hospital Reports Analysis 
1.  Older patients are more likely to have positive test results. From the research analysis older adults in the age class of 45-64 were tested positive which was about 24,000 then follow by age class 65+ which was about 20,000 people were tested positive. However, older adults have the tendency of reacting positive to the results because of the ageing body system.
   
2.  There are very clear and substantial difference in CK-MB and Troponin levels between positive and negative results.  CK-MB levels results vary, about 94% of the patients were tested positive while 6% of the patients were tested negative.
   
3.  The gender distribution across positive and negative results appears somewhat balanced, but there are more positive cases for male gender than female gender.  they were gender differences in the test results for the female patients only 247 were tested positive and 202 patients were tested negative. For the male patients only 563 were tested positives and 307 were tested negatives.
  
4.  The heart rate, systolic blood pressure and blood sugar, the average values and distribution are quite similar between positive and negative result groups.  High blood sugar correlate with positive test results which was estimated to 117,000 compares with the negative blood sugar test which was about 76,000.
  
5.  Troponin and CK-MB level varies across different age classes but its peak was at the age class 45-64 with troponin 288.48 and CK-MB 9,456.23 followed by age class 65+ with troponin 166.85 and CK-MB 6,575.85. both the troponin and CK-MB level values dropped at the age class 14-24 with troponin 3.59 and CK-MB level 411.03.







## DISCUSSION

**INTERPRETATION OF RESULTS**
 

 
 
















## CONCLUSION

The research clearly demonstrates that CK-MB and Troponin are the most crucial and differentiating biomarkers in determining a positive medical test result. Patients exhibiting positive results consistently present with significantly elevated levels of both CK-MB and Troponin, while negative results are associated with very low levels of these markers. This strong association underscores their paramount importance as indicators for the underlying medical condition being tested.

While age shows a modest tendency for positive results in older individuals and other vital signs (heart rate, blood pressure, blood sugar) are important for overall health, their direct correlation with the positive test outcome is not pronounced as that of cardiac biomarkers. It is advisable that patients should maintained the standard benchmark of both systolic and diastolic blood pressure standard of 120/80mmHg and anything above that they should visit medical centers. 




















## RECOMMENDATION

Based on these findings, here are some recommendations for the research
1.  **Prioritize Cardiac Biomarkers for Diagnosis:** Given the clear and significant association, CK-MB and Troponin levels should be considered primary diagnostic markers for the condition indicated by positive test results.

2.  **Consider Age as A Risk Factor:** The trend for positive results occurring more frequently in older individuals suggests age should be considered a contributing risk factor. Health practitioners should have a heightened awareness for older patients presenting with relevant symptoms.

3. **Maintain Holistic Patient Assessment:** By monitoring heart rate, blood pressure, blood sugar are fundamental to overall cardiovascular health assessment. Continuous monitoring of these vital signs is crucial for comprehensive patients care, as abnormalities can indicates underlying health issues that may indirectly affect the patients.

4.  **Further Investigative Gender Differences:** While difference was observed in the number of positive cases across genders, further statistical analysis is needed to determine if this difference is statically significant. If confirmed, targeted screening or prevention strategies could be explored based on gender.

5.  **Refine Future Data Collection:**  For future research, consider collecting additional information, such as specific symptom’s, medical history (e.g., pre-existing conditions like diabetes or hypertension), and lifestyle factors. This could provide a more comprehensive understanding of the positive result and enable the development of more personalized risk profiles.


