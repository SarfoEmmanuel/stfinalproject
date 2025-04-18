# Final Slightly Techie Project
# Caramel Data Analytics

# PROJECT OVERVIEW
**Unravelling the Challenges of Healthcare Accessibility in Africa: A Case Study Primary Goal**
This case study aims to analyze healthcare facility data, identify disparities in access to healthcare between rural and urban regions, and evaluate the efficiency of healthcare funding. The objective is to propose data-driven recommendations that governments and stakeholders can implement to enhance healthcare service delivery across Africa.

# Data Overview  
1. Rural vs. Urban Healthcare Disparities: This dataset provides insights into the distribution of healthcare facilities, the number of doctors and nurses, and patient accessibility across different regions. 
2. Healthcare Workforce Availability: This dataset includes information on the availability of doctors and nurses per facility and how this varies between urban and rural locations. 
3. Patient Accessibility and Utilization: The dataset tracks annual patient visits, average distance to facilities, and emergency response times, helping assess accessibility in different regions. 
4. Funding and Resource Allocation: This dataset explores the funding received by healthcare facilities and their access to essential services like electricity and the internet. 
5. Patient Satisfaction and Healthcare Outcomes: Patient satisfaction rates serve as indicators of service quality, while other factors like emergency response times help evaluate healthcare system efficiency. 

**Key Business Questions**
1. How does the distribution of healthcare facilities compare between rural and urban regions? 
2. Are urban healthcare facilities receiving more funding than rural ones? 
3. Are healthcare facilities with higher funding more likely to have shorter emergency response times? 
4. Which facility types (hospitals, clinics, health centers) show the highest efficiency in terms of funding per patient visit? 
Actionable Insights for Stakeholders 
5. What are the critical factors preventing equal access to healthcare across different regions? 
6. Which policy recommendations can be made to bridge the gap between urban and rural healthcare services? 
7. How can governments optimize healthcare funding allocation to maximize impact in underserved regions? 

**Expected Outcomes**
1. Identify key disparities in healthcare access between rural and urban regions. 
2. Analyze the efficiency of healthcare funding and resource allocation across different facilities. 
3. Provide data-driven insights to improve emergency response times and patient satisfaction. 
4. Develop strategic recommendations for policymakers to ensure equitable healthcare access. 
5. Use data visualization techniques to communicate your findings effectively to stakeholders.


# Link to dataset: Healthcare Accessibility in Africa Case Study Datasets
+ https://github.com/SarfoEmmanuel/stfinalproject/blob/a22ef1cf96903854a04721e9beff5f25550c5c2c/healthcare_africa.csv

# Link to Visualization in Power BI Format
+ https://github.com/SarfoEmmanuel/stfinalproject/blob/538cac6ec415bbc60ba49549973eea36af546b04/Healthcare%20Access.pbit

# Code for the Entire Project With Visualization
+ [DataAnalysis.ipynb](https://github.com/SarfoEmmanuel/stfinalproject/blob/3a23243fdfdb6ca5db6082a7272ea4e9dd7be6ad/DataAnalysis.ipynb)

# Code for the Entire Project Without Visualization
DataAnalysis.py

# Requirements
+ Anaconda
+ JupyterNotebook

**Libraries**
+ Pandas
+ Numpy
+ Matplotlib
+ Seaborn

**Sklearn**
* train_test_split
* RandomForestRegressor
* r2_score, mean_absolute_error, mean_squared_error
* LabelEncoder

# Importing Libraries
+ Now let’s start the task of understanding the dataset by importing the necessary Python libraries and the dataset:
![image](https://github.com/user-attachments/assets/4274fb13-3d97-4ace-b707-2b5107520d0a)

# Storing the variables in a dataframe and reading the df to check if it's imported successfully
![image](https://github.com/user-attachments/assets/01a9c745-c0a8-479b-ada8-68cc0b298d14)

# Exploration of the data
Now your goal is to explore the dataset to understand what it contains
+ ![image](https://github.com/user-attachments/assets/c4dfa573-e3fc-4a63-87da-c2aa3278ac22)

# Below is the complete description of this dataset:
Data columns (total 15 columns):
+   Column                             Non-Null Count  Dtype  
---  ------                             --------------  -----  
+ 0   Region                             2000 non-null   object 
+ 1   Country                            2000 non-null   object 
+ 2   Population                         2000 non-null   int64  
+ 3   Facility Name                      2000 non-null   object 
+ 4   Facility Type                      2000 non-null   object 
+ 5   Number of Beds                     2000 non-null   int64  
+ 6   Number of Doctors                  2000 non-null   int64  
+ 7   Number of Nurses                   2000 non-null   int64  
+ 8   Annual Patient Visits              2000 non-null   int64  
+ 9   Emergency Response Time (minutes)  2000 non-null   int64  
+ 10  Funding Received (USD)             2000 non-null   int64  
+ 11  Electricity Availability           2000 non-null   object 
+ 12  Internet Availability              2000 non-null   object 
+ 13  Patient Satisfaction Rate (%)      2000 non-null   float64
+ 14  Average Distance to Facility (km)  2000 non-null   float64
+ dtypes: float64(2), int64(7), object(6)

+ **more description**
![image](https://github.com/user-attachments/assets/0cd363c4-86db-4600-9910-1f9f4f77f920)



# Classifying Areas into Rural and Urban Areas
Now, to explore the dataset and draw a conclusive analysis, we need to add a new column called Area Type, which we would separate based on Internet Availability, Electricity, Population Size and Average Distance to Facility (km)
![image](https://github.com/user-attachments/assets/aac931f9-585f-42f5-8858-7cc6d3682a2e)


+ Checking if the New Column has been added to the dataframe
![image](https://github.com/user-attachments/assets/26d8d4a3-391a-45de-954d-44f417412ea8)

# Understanding Key Business Questions
+ # How does the distribution of healthcare facilities compare between rural and urban regions?
To know the distribution of healthcare facilities across rural and urban regions, we need to count the number of facilities available
![image](https://github.com/user-attachments/assets/a0806a93-5569-4043-ad07-9df06352a517)


+ **Visualizing it**
![image](https://github.com/user-attachments/assets/bc45babe-6370-4569-8f3c-a77675ee4111)

# Are urban healthcare facilities receiving more funding than rural ones? 
![image](https://github.com/user-attachments/assets/658bffc9-85a1-42c6-8e07-df6744fa65fa)

+ **Visualizing it**
![image](https://github.com/user-attachments/assets/2b571b2e-8e8a-45df-866d-fe93282e158a)

![image](https://github.com/user-attachments/assets/0701a6f2-deab-406e-a5d1-b6c7bef1f2c1)


# Are healthcare facilities with higher funding more likely to have shorter emergency response times?
To understand if facilities with higher funding are more likely to have shorter emergency response times, we need to know the funding in each facility
![image](https://github.com/user-attachments/assets/a76f70b5-1419-465d-8ec6-a7618e220671)

+ **Visualizing it**
![image](https://github.com/user-attachments/assets/ca3a7941-c01f-46f5-a5c2-86c9fe1ec180)

![image](https://github.com/user-attachments/assets/d2d910f8-acf1-4851-8e2c-e86e7248d0b5)

![image](https://github.com/user-attachments/assets/723b85fb-e168-4dce-8d24-a55c506ffa18)

**Analyzing facilities with respect to funding and emergency response**
![image](https://github.com/user-attachments/assets/ef508bec-0f75-4d3b-8545-6981687905ef)

![image](https://github.com/user-attachments/assets/d5ba0d43-07fb-4abf-b6c6-a0cb80159a54)

# Which facility types (hospitals, clinics, health centers) show the highest efficiency in terms of funding per patient visit? 
![image](https://github.com/user-attachments/assets/04be4780-46c3-4b7e-bb5d-26013c82e8bb)
![image](https://github.com/user-attachments/assets/d488676c-5e12-4608-9a63-822c24f729d0)


