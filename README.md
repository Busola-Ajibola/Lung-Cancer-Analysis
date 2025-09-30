##                                                                Lung-Cancer-Analysis
This report aims to analyze the data related to lung cancer. Lung cancer is a major contributor to cancer-related deaths making the study of its epidemiology and treatment outcomes paramount. 
## 1.	INTRODUCTION
This dataset offers an in-depth look at various factors linked to lung cancer diagnosis and management. It contains essential information regarding patient demographics, clinical histories, and treatment outcomes, allowing researchers and healthcare providers to better understand the disease's prevalence and development.

##	OBJECTIVES
I.	To examine the influence of age, gender, and country of residence on lung cancer diagnosis and treatment outcomes.
II.	To explore the effects of comorbid conditions (such as hypertension, asthma, and cirrhosis) on treatment efficacy and patient survival.
III.	To determine the role of family history in lung cancer risk and its implications for early diagnosis and intervention.
IV.	 ⁠To assess the effectiveness of different treatment types, including surgery, chemotherapy, and radiation therapy, on patient survival rates.
V.	⁠To investigate how body mass index (BMI) and cholesterol levels relate to lung cancer progression and treatment success.

##	SCOPE
This report will specifically examine key variables including;
I.	Demographic Variables:
• Age: Age of the patient at diagnosis.
• Gender: Gender of the patient.
• Country: Country of residence of the patient. 

II.	Clinical Variables:
• Diagnosis Date: Date when lung cancer was diagnosed.
• Cancer Stage: Stage of cancer at the time of diagnosis.
• Family History: Presence of lung cancer in the family.

III.	Lifestyle Factors:
• Smoking Status: Current or past smoking habits.
• BMI: Body Mass Index of the patient.
• Cholesterol Level: Cholesterol levels measured.

IV.             Comorbid Conditions:
Hypertension: Presence of high blood pressure.
Asthma: History of asthma.
 Cirrhosis: Presence of liver cirrhosis.

 V.             Treatment Variables:
• Treatment Type: Type of treatment received (e.g., surgery, chemotherapy).
• End Treatment Date: Date when treatment concluded.

VI.	Outcome Variable:
• Survived: Indicator of whether the patient survived beyond a specified follow-up period.                                                                                                             

## KEY COLUMNS

•	ID: The unique identifier (ID) for each patient.
•	 Age: The age of the patient at the time of diagnosis.
•	 Gender: The gender of the patient, which may influence cancer risk and treatment outcomes.
•	 Country: The country of residence, reflecting geographical variations in lung cancer incidence and treatment practices.
•	Diagnosis Date: The date when the lung cancer diagnosis was made.
•	Cancer Stage: The stage of cancer at diagnosis, which is crucial for determining treatment options and prognosis.
•	Family History: Information on whether there is a family history of lung cancer, which may indicate hereditary risk factors.
•	 Smoking Status: A record of the patient's smoking habits, an established risk factor for lung cancer.
•	 BMI: Body Mass Index, which can impact overall health and treatment efficacy.
•	 Cholesterol Level: Levels of cholesterol, which may have associations with cancer progression.
•	Hypertension: Information on whether the patient has hypertension, potentially affecting treatment options.

•	 Asthma: History of asthma in the patient, which may influence lung health and cancer risk.
•	 Cirrhosis: Presence of cirrhosis, which can complicate treatment and outcomes.
•	 Treatment Type: The type of treatment administered, including surgery, chemotherapy, or radiation therapy.
•	End Treatment Date: The date when the treatment concluded, providing insight into treatment duration and management.
•	Survived: A binary indicator of whether the patient survived beyond a specified follow-up period.
•	Age group: A classification that divides individuals into ranges based on their age. 
•	 ⁠Cholesterol level: A categorization indicating the levels of cholesterol in the blood stream. It could either be high or low. 
•	⁠Number of days treatment: The total duration, measured in days, that a patient has been undergoing a specific treatment for a condition. This can indicate the length of therapy and may correlate with treatment outcomes.
•	⁠Weight: The measure of how heavy an individual is. It is an important metric in assessing health and treatment responses.

## 2.	DATA CLEANING PROCESS
I.	Removing duplicates
                  We used this syntax “drop_duplicates() “ to check for duplicates and remove any duplicate rows. 
II.	Checking data types
    We used this syntax “data.dtypes” to show the data type of each column in the DataFrame. This is done to ensure that each column in  the DataFrame has the correct data type and this helps to prevent errors during analysis.
III.	Checking null values
                     We used this syntax “data.isna().sum() “ to identify missing values in the data set. Missing values can lead to inaccurate analysis or model performance.
IV.	Checking unique values
                     We used the syntax “data.unique() “ to return the count of unique values in the specified column. This is done to understand the number of unique entries in each column, which can help in identifying categorical variables and potential anomalies.

## 3.	Key insights from the analysis of lung cancer data set
3.1	The most common age group affected by cancer
Analysis: We categorized the age group into the following categories; children, teenagers, adults and the old.
Insights: The prevalence of cancer among different age groups shows the following significant variation: The most common age group affected by cancer is adults. They have the highest incidence, with 597,823 cases, indicating that they are predominantly affected by cancer. The old has 290,742 cases, reflecting the increased cancer risk associated with the age. Teenagers have significantly fewer cases at 1,401, indicating that cancer in this age group is rare. Also, the children have the lowest incidence, with only 35 cases reported.

3.2	the survival rate across all age groups
Analysis: we compared survival rate across all the age groups to know if age have an impact on survival.
Insights: the survival rates by age for Old 226,550 (77.9%) confirmed dead, 64,192 (22.1%) survived. Adult 466,342 (78%) confirmed dead, 131,480 (22%) survived. Teenagers 1,077 (76.9%) confirmed dead and 324 (23.1%) survived. Children 27 (77.14%) confirmed dead, 8 survived (22.86%). This suggests that adult has the highest death rate with 78% while Teenagers has the highest survival rate with 23.1%.

3.3	The cancer rates by gender 
Analysis: We compared the cancer rates using statistical methods for male and female patients.
Insights: The cancer rates by gender indicates that males are slightly more affected by cancer, with 445,134 cases reported, compared to females, who have 444,866 cases. This suggests that cancer impacts males marginally more than females in this dataset.

3.4	The Survival rates by gender
Analysis: we compared the survival rates using statistical methods for male and female patients.
Insights: The survival rates by gender indicates that 347,034 (77.98%) female patients were confirmed dead while 97,832 (22.02%) survived, for male patients 346,962 (77.92%) confirmed dead while 98,172 (22.08%) survived. This suggests more male patients survived cancer and more female patients were confirmed dead


3.5	The most common country affected by cancer
Analysis: We counted number of cancer cases by country.
Insights: Malta has the highest incidence recording 33367 cases followed closely by Ireland having 33243 cases and Portugal having 33208.Also, Bulgaria has the lowest case of cancer recorded having 32559 cases.

3.6	The most common treatment type
Analysis: We grouped patients by treatment types.
Insights: The most common treatment type is chemotherapy. Chemotherapy emerges as the most prevalent treatment option, with 223,262 cases. This treatment involves using drugs to kill or inhibit the growth of cancer cells and is often combined with other modalities for enhanced effectiveness. Following closely is surgery, reported in 223,261 cases, which involves physically removing tumors or cancerous tissue. Additionally, the data includes 222,609 cases categorized under combined treatments, where multiple modalities, such as chemotherapy alongside surgery or radiation, are employed. The least common treatment type is Radiation recording 220,868 cases.

3.7	treatment type and their survival rate 
analysis: the treatment type and the impact on survival.
Insights: the survival rate by treatment type shows that chemotherapy had 48,836 (21.87%) survivals and 174,426 (78.13%) deaths. Combined had 49,002 (22.01%) survivals and 173,607 (77.99%) deaths. Radiation had 48,714 (22.06%) survivals and 172,154 (77.94%) deaths and Surgery had 49,452 (22.15%) survivals and 173,809 (77.85%) deaths. This suggests that Surgery has the highest survival rate with 22.15% and chemotherapy has the highest death rate with 78.13%.

3.8	The smoking status of patients.
Analysis: patients and their smoking records
Insights: the cancer rate by smoking status indicates that Passive smokers are 223,170, Never Smoked are 222,751, Former Smokers are 222,181 and Current Smokers are 221,898 patients. 
3.9	Smoking status and its impact on survival.
Analysis: the smoking status and their survival rate across all patients.
Insights: the survival rate by smoking status shows that passive smokers have 174,067 (77.96%) deaths and 49,103 (22.04%) survivors, Never Smoked has 173,543 (77.87%) Deaths and 49,208 (22.13%) survivors, Former smokers have 173,381 (77.99%) deaths and 48,800 (22.01%) survivors, Finally Current Smokers has 173,005 (77.93%) deaths and 48,893 (22.07) survivors. This suggest patient who has never smoked have a high possibility of surviving with the highest surviving rate of 22.13% and patients who are former smokers has highest death rate with 77.99% followed my passive smokers with a rate of 77.96%.

3.10	The percentage of patients with a family history of cancer
Analysis: We calculated the percentage of patients who report a family history of cancer.
Insights: The data reveals important insights into the relationship between family history of cancer and lung cancer cases. Among the patients assessed, those with a family history of cancer total 444,819 (49.98%) cases. This figure suggests that a significant portion of lung cancer patients may have a genetic predisposition or familial links to cancer, which can influence their risk levels. In contrast, the number of patients with no family history of cancer is slightly higher, totaling 445,181 (50.02%) cases. This indicates that while a family history is a relevant factor, a substantial number of lung cancer patients do not have such a background.

3.11	The analysis of cholesterol levels of patients
Analysis: We categorized the cholesterol status into three (3) different groups; The low cholesterol status, the medium cholesterol status and the high cholesterol status.
Insights: This data indicates that a significant majority of lung cancer patients have high cholesterol levels, which raises important considerations for patient management. Patients with low cholesterol status total 237,408 (26.67%) cases, while Patients with medium cholesterol status account for 197,668 (22.21%) cases. This group represents a middle ground in cholesterol levels. In conclusion, patients with high cholesterol status show the highest count, with 454,924 (51.12%) cases.

3.12	The analysis of cancer stages of patients 
Analysis; there are 4 cancer stages with stage I having 222,516, stage II having 222,363, stage III having 222,594 and stage IV having 222,527 Patients.
Insights: the survival rate by cancer stages shows that stage I has 173,978 (78.14%) deaths and 48,538 (21.86%) survivors, stage II has 173,245 (77.86%) Deaths and 49,118 (22.14%) survivors, stage III has 173,506 (77.92%) deaths and 49,088 (22.08%) survivors, finally stage IV has 173,267 (77.84%) deaths and 49,260 (22.16%) survivors. This shows that patients with stage IV have the highest rate of survivors with 22.16% and patients with stage I cancer has the highest death rate which is 78.14%.



3.13	The weight analysis of patients
Analysis: We categorized the weight status of the patients into four (4) different groups; The normal weight, obese, overweight and underweight.
Insights: The patients with normal weight recorded 199,482 (22.41%) cases. This group represents those whose weight falls within a healthy range according to standard body mass index (BMI) classifications. The obese patients recorded 612,679 (68.84%) cases, which is the largest number of cases recorded in the dataset. Patients that are overweight account for 2,531 (0.28%) cases. This group is significantly smaller and indicates that fewer patients fall into this category. In conclusion, the patients classified as underweight recorded 75,308 (8.46%) cases.

3.14	The analysis of how conditions like asthma, cirrhosis, Hypertension and other cancer affect survival outcomes
Analysis: the dataset contains patients with other diseases such as asthma, cirrhosis and other cancer which could also affect the chance of survival of patients.
Insights: the total patients with asthma are 418,069 which 91,738 survived and 326,331 died. For cirrhosis the total number of patients with cirrhosis are 201,101 with 156,511 deaths and 44,590 survivors and finally patients or had other cancers apart from lung cancer are 78,460 with 61,387 deaths and 17,073 survivors.

## 4.	Recommendations
4.1	The most common age group affected by cancer (Adults)
•	Implement targeted cancer screening programs for adults, especially in workplaces and community health centres.
•	Promote lifestyle modification campaigns (healthy diet, exercise, reduced alcohol/tobacco) aimed at the adult population.
•	Increase awareness of early detection signs among adults through educational programs and media campaigns.
4.2	Survival rate across all age groups
•	Investigate why teenagers have slightly higher survival rates identify protective factors and replicate in other groups.
•	Improve access to advanced treatment and follow-up care for adults and older patients, where death rates are highest.
•	Integrate palliative care and psychological support for high-risk age groups to improve quality of life and treatment adherence.

4.3	Cancer rates by gender
•	Design gender-sensitive cancer prevention strategies, ensuring outreach programs address both male and female needs equally.
•	Encourage men to undergo regular screening, as they have a marginally higher incidence rate.
•	Fund studies into gender-related biological and behavioural risk factors.

4.4 Survival rates by gender
•	Investigate clinical and social reasons why female patients show slightly higher mortality despite similar case numbers.
•	Encourage gender-specific support groups and survivorship programs to improve coping and recovery.
•	Standardize treatment guidelines to ensure equity in medical interventions.

4.5 Most common country affected by cancer (Malta)
•	Conduct environmental and lifestyle risk factor studies in Malta, Ireland, and Portugal to identify underlying causes.
•	Strengthen cancer registries and early detection infrastructure in high-incidence countries.
•	Share best practices from lower-incidence countries like Bulgaria to reduce cases in high-incidence regions.

4.6 Most common treatment type (Chemotherapy)
•	Expand research into improving chemotherapy effectiveness while reducing side effects.
•	Educate patients on treatment options, ensuring informed decision-making about combinations of surgery, chemo, and radiation.
•	Allocate funding for innovations in targeted therapies to complement chemotherapy.

4.7 Treatment type and survival rate
•	Investigate why surgery shows slightly better survival rates and consider expanding surgical access where feasible.
•	Personalize treatment selection using genetic profiling to assign patients to the most effective modality.
•	Integrate multi-disciplinary treatment approaches to optimize outcomes.

4.8 Smoking status of patients
•	Launch aggressive anti-smoking and second-hand smoke prevention campaigns, given the high number of passive smokers.
•	Strengthen tobacco control laws and workplace smoke-free policies.
•	Provide free cessation support programs for current and former smokers.

4.9 Smoking status and survival
•	Target former and passive smokers with intensive follow-up and monitoring, as they show higher death rates.
•	Develop preventive programs for non-smokers to maintain their lower-risk profile.
•	Include smoking history in personalized treatment planning.

4.10 Family history of cancer
•	Encourage genetic testing and counselling for patients with a family history of cancer.
•	Implement early screening programs for high-risk families.
•	Promote lifestyle and preventive measures to reduce modifiable risks even in genetically predisposed groups.

4.11 Cholesterol levels of patients
•	Investigate potential biological links between high cholesterol and cancer incidence.
•	Integrate cholesterol monitoring into cancer screening programs.
•	Promote dietary and lifestyle changes to control cholesterol as part of cancer prevention.



4.12 Cancer stages and survival
•	Enhance public education on early cancer detection to reduce late-stage diagnoses.
•	Improve access to advanced treatments for Stage I patients, where death rates are unexpectedly high.
•	Strengthen follow-up and rehabilitation programs for Stage IV survivors.

4.13 Weight analysis of patients
•	Prioritize obesity prevention programs through nutrition education, physical activity promotion, and community health initiatives.
•	Monitor underweight patients for potential underlying illnesses that may increase cancer vulnerability.
•	Implement workplace wellness programs to help adults maintain healthy BMI ranges.

4.14 Other conditions affecting survival
•	Integrate multi-disease management programs for patients with cancer and comorbidities like asthma, cirrhosis, and other cancers.
•	Provide specialized care pathways for high-risk comorbid patients to improve survival outcomes.
•	Train healthcare providers to coordinate care between oncology and other specialties.

## 5.	CONCLUSION
This analysis provides a comprehensive overview of the factors influencing cancer incidence and survival across different demographic, lifestyle, and clinical categories. Adults bear the highest disease burden, while teenagers demonstrate relatively better survival outcomes. Gender differences are marginal, though males are slightly more affected and females experience slightly higher mortality. Geographic disparities are evident, with certain countries showing notably higher incidence rates.

Treatment analysis reveals that while chemotherapy remains the most common approach, surgical intervention shows a modest survival advantage, highlighting the need for individualized treatment planning. Lifestyle factors such as smoking status, obesity, and high cholesterol significantly correlate with cancer risk and outcomes, underlining the importance of preventive health strategies. Stage specific survival patterns reaffirm the critical role of early detection, and comorbid conditions like asthma, cirrhosis, and other cancers further underscore the necessity for integrated, multi-disciplinary patient care.

Overall, the findings emphasize that effective cancer control requires a multi-pronged strategy combining prevention, early diagnosis, personalized treatment, and coordinated management of comorbidities to reduce incidence, improve survival rates, and enhance quality of life for patients across all populations.


<img width="468" height="647" alt="image" src="https://github.com/user-attachments/assets/c26f8327-7878-48c1-982b-57858daf6e86" />
