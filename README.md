# CodeMonk-MLTest

# Task 1 - EDA (Insights)

1. Preprocessing :
- Data has a high presence of outliers which could severly affect analysis. In this case, I have applied sqrt_transformations in an attempt to reduce skewness for production values.
- The data entries with missing values in production were dropped since they only mounted to around 3,000 entries out of the dataset of more than 2,00,000. Otherwise, a median value substitution is suggested to ensure robustness to outliers.

2. Highest Production :
- State : Kerala
- District : Kozhikhode
- Year : 2011
- Season : Whole Year followed by Kharif
- Crop : Coconut 
   
3. (State) Use Case : State of Uttar Pradesh
   (based on highest production)
- Best District : Kheri
- Best Year : 1997
- Best Season : Kharif
- Best Crop : Sugarcane
   
4. (Year) Use Case : 2003 
   (based on highest production)
- Best Season : Whole Year
   
5. (Crop) Sample Use Case : Coconut 
   (based on highest production)
- Best Season : Whole Year 
   
6. Comments :
- For the relationship between Area and Production, an inversely proportional relationship is observed by graph although this can heavily vary based on the innate relationship between crops grown and seasons across years. (eg. for Coconut, the relation seems directly proportional.)
- Coconut is be the most produced crop because it can be produced for the whole year in most states.
- Further EDA for the dataset would differ as per requirements and can be easily obtained with the help of the use cases.


# Task 2 - EDA (Insights)
1. Preprocessing : 
- Few null values were observed in five columns and the corresponding data entries were discarded.
- The data showed minimal to no signs of outliers since variables were categorical.
 
2. Highest number of products in each variable :
- Gender : Men
- masterCategory : Apparel
- subCategory : TopWear
- articleType : Tshirts
- baseColour : Black
- Season : Summer
- Year : 2012
- Usage : Casual
- productDisplayName : Lucera Women Silver Earrings

3. Highest number of products across genders in masterCategory : Apparel for Men

4. Highest number of products across seasons in masterCategory : Apparal for Summer

5. Highest number of products across colours in for genders :
- Boys : Blue (159)
- Girls : Pink (167)
- Men : Black (5874)
- Unisex : Black (761)
- Women : Black (2941)

8. Highest number of products across colours in masterCategory : Black for Accessories

9. (Colour) Sample Use Case : Black
- Gender : Men
- Season : Summer

10.(masterCategory) Sample Use Case : Personal Care
- Year : 2017
- Gender : Women

11.Comments : 
- Black can be called the most popular colour amongst men and women for summer.
- Personal Care products were only introduced in the market 2017.
- Further EDA for the dataset would differ as per requirements and can be easily obtained with the help of the use cases.
