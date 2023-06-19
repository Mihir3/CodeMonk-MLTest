# CodeMonk-MLTest

# Task 1 - EDA (Insights)

# Preprocessing :
 - Data has a high presence of outliers which could severly affect analysis. In this case, I have applied sqrt_transformations in an attempt to reduce skewness for production values.
- The data entries with missing values in production were dropped since they only mounted to around 3,000 entries out of the dataset of more than 2,00,000. Otherwise, a median value substitution is suggested to ensure robustness to outliers.

# Highest Production :
   State : Kerala
   District : Kozhikhode
   Year : 2011
   Season : Whole Year followed by Kharif
   Crop : Coconut 
   
#  (State) Use Case : State of Uttar Pradesh
   (based on highest production)
   Best District : Kheri
   Best Year : 1997
   Best Season : Khrif
   Best Crop : Sugarcane
   
#  (Year) Use Case : 2003 
   (based on highest production)
   Best Season : Whole Year
   
#  (Crop) Sample Use Case : Coconut 
   (based on highest production)
   Season : Whole Year 
   
# Comments :
1. For the relationship between Area and Production, an inversely proportional relationship is observed by graph although this can heavily vary based on the innate relationship between crops grown and seasons across years. (eg. for Coconut, the relation seems directly proportional.)
2. Further EDA for the dataset would differ as per requirements and can be easily obtained with the help of the use cases.
