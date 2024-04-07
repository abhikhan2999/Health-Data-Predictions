# **Data Analysis, Observations and Recomsndations**

## **1. Analysis of Adolescent Obesity dataset**
 - 1.1 This file contains 43 entries with 4 Columns:-
   - Location : State in USA
   - VAlue : Peecent Value Sample
   - 95 % Cl : Confidence Interval Values Ranging from and to 
   - Sample Size : The Size of the sample
  
 -  1.2 Null Values : We have no null values in the dataset

## **2. Analysis of Adult Obesity dataset**
 - 2.1 This file contains 55 entries with 4 Columns:-
   - Location : State in USA
   - VAlue : Peecent Value Sample
   - 95 % Cl : Confidence Interval Values Ranging from and to 
   - Sample Size : The Size of the sample
 -  2.2 Null Values : We have no null values in the dataset
## **3. Analysis of Nutrition Obesity dataset**
 - 3.1 This file contains 35042 entries with 14 Columns:-
   - 'YearStart' : Start of survey 
   - 'YearEnd' : End of Survey
   - 'LocationAbbr' : Location at survey carried out
   - 'State' : State survey carried out
   - 'Class' : Class for which survey is carried out i.e Obesity / Wt
   - 'Question' : Questions asked like how many percent in class has obesity
   - 'Data_Value_Type' : Data Type
   - 'Data_Value' : Data Value 
   - 'Low_Confidence_Limit' : Lower limit of confidence 
   - 'High_Confidence_Limit ' : Lower limit of confidence 
   - 'Sample_Size' : Size of people sample
   - 'Gender' : Sex
   - 'Grade' : Class of study
   - 'Race_Ethnicit : Race of the sample
 -  3.2 Null Values : We have fol values in the dataset:-
    - Gender                    30036
    - Grade                     25030
    - Race_Ethnicity            17521
    - Data_Value                 9309
    - Low_Confidence_Limit       9309
    - High_Confidence_Limit      9309
    - Sample_Size                9309  
-   3.4 Handling of Missing values in the dataset:-
    -  Since we know that in this dataset our values lies between the Data Value, upper and Lower confidence level. So in the dataset if all these three features are missing then they are not required and imputing these values may give us wrong insights about the dataset, as these are the main features.
    -  As we found that the missing values in each column are more than 50% so it is not good practice to impute them.So we have dropped the Columns, Race_Ethinicity, Gender and Class
    -  3.5 Encoding of Categorical Values:
    -  **Question Column**
       -      'Percent of students in grades 9-12 who have obesity': 1,
       -      'Percent of students in grades 9-12 who have an overweight classification': 2,
       -      'Percent of students in grades 9-12 watching 3 or more hours of television each school day': 3,
       -      'Percent of students in grades 9-12 who consume fruit less than 1 time daily': 4,
       -      'Percent of students in grades 9-12 who participate in daily physical education': 5,
       -      'Percent of students in grades 9-12 who consume vegetables less than 1 time daily': 6,
       -      'Percent of students in grades 9-12 who drank regular soda/pop at least one time per day': 7,
       -      'Percent of students in grades 9-12 who achieve 1 hour or more of moderate-and/or vigorous-intensity physical activity daily': 8
    -  "**Class Column**"
       -      'Obesity / Weight Status': 1,
       -      'Fruits and Vegetables': 2,
       -      'Physical Activity': 3,
       -      'Television Viewing': 4,
       -      'Sugar Drinks': 5
  - 3.6 Outliers Removal / Scaling of the dataset
    - All the outlires are visualize thorugh BoxPlot and then removed using IQR Method with 1.5 x Time upper and Lower Limit to the dataset
    - The Data is scaled with MinMax Scler so, that the computuiona Time and cost is decreased and the Accuracy of the model is increased.


- 3.7 Final Results of the Nutrition Obesity after applying the linear Model 
  - Root Mean Squared Error : 0.35
  - R_Squared Value         : 0.99


## **4. Analysis of Weight Obesity dataset**
 - 4.1 This file contains 2899 entries with 17 Columns:-
   - 'unit': wether data is age oriented or not
   - 'classification1' :  Sex and race and Hispanic origin, Sex and age ,Percent of poverty level, Race and Hispanic origin, Sex, Total,  
   - 'demographic_group', 'year', 'estimate',
   - 'grade 1 obesity (bmi from 30.0 to 34.9)' : GradeI Obesity
   - 'grade 2 obesity (bmi from 35.0 to 39.9)' : GradeII Obesity
   - 'grade 3 obesity (bmi greater than or equal to 40.0)' : GradeIII Obesity
   - 'normal weight (bmi from 18.5 to 24.9)' : GradeIV Obesity
   - obesity (bmi greater than or equal to 30.0)' : GradeV Obesity
   - 'overweight or obese (bmi greater than or equal to 25.0)' : GradeVI Obesity
   - 'age_20-34 years', 'age_35-44 years', 'age_45-54 years' : GradeVII Obesity
   - 'age_55-64 years', 'age_65-74 years', 'age_75 years and over' : GradeVIII Obesity

- 4.2 Encode the dataset, clean the data, outlier detection and removal followed by scaling of the data as done in prevous dataset.
    - Add new columns start of the year and end of the year for better handling of the dataset
    - Drop the year column
    - Encode the demographic_group column
    - Encode the classification1 column
    - Encode the unit column
    - Remove the outliers from the dataset
    
    
- 4.5 Machine Learning Models for Classification Problem
    - Linear Regression (Accurcay Score Acheived = 1)
    - Random Forest Classifier (Accurcay Score Acheived = 1)
    
    
    
## 5. **Conclusions and Recommendations:**

### 5.1 Adolescent Obesity Dataset:
   - **Conclusion:** The dataset provides information on obesity rates among adolescents in different states of the USA.
   - **Recommendation:** Further analysis should be conducted to identify patterns and trends in adolescent obesity rates, which can help in implementing targeted interventions and programs to address the issue.

### 5.2 Adult Obesity Dataset:
   - **Conclusion:** The dataset contains information on obesity rates among adults in different states of the USA.
   - **Recommendation:** Conduct in-depth analysis to understand the prevalence of adult obesity in different states and develop strategies and policies to promote healthy lifestyles and combat obesity.

### 5.3 Nutrition Obesity Dataset:
   - **Conclusion:** The dataset includes a large number of entries and provides information on obesity, diet, and physical activity.
   - **Recommendation:** Due to significant missing values, caution should be exercised when imputing data. Focus on available information and conduct analyses to explore factors associated with obesity and their impact on different population groups.

### 5.4 Weight Obesity Dataset:
   - **Conclusion:** The dataset provides information on obesity rates categorized by demographic groups, age ranges, and classifications.
   - **Recommendation:** Conduct detailed analysis to explore obesity rates across different demographic groups, age ranges, and classifications. Apply machine learning models to predict obesity rates and identify important predictors.

## 6. **General Recommendations:**
- Conduct comprehensive studies using the available data to gain insights into the causes and consequences of obesity.
- Collaborate with healthcare providers, policymakers, and researchers to develop targeted interventions and policies to address obesity.
- Promote awareness campaigns to educate the public about the importance of a healthy lifestyle and the risks associated with obesity.
- Implement programs that focus on nutrition education, physical activity promotion, and access to healthy food options.
- Evaluate the effectiveness of interventions and make necessary adjustments based on the findings.
- Continuously monitor obesity rates and trends to assess the impact of interventions and identify areas that require further attention.
- Foster interdisciplinary collaborations to tackle obesity from multiple angles, including healthcare, education, urban planning, and policy-making.
- By following these recommendations, it is possible to make significant progress in addressing the obesity epidemic and improving public health outcomes.
