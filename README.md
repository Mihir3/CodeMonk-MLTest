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
- Personal Care products were only introduced in the market in 2017.
- Further EDA for the dataset would differ as per requirements and can be easily obtained with the help of the use cases.

# Task 2 - Model

The model was built in Tensorflow because of my relative familiarity with the framework instead of Pytorch.

The data entries with missing values in any variable were dropped.

In my first attempt, for the fashion dataset, since the images were of low resolution with easy distinguishable classes, I wrote a simple Convolutional Neural Network with four convolutional layers. For the model, because of 44k images, the training crashed multple times, hence I made the assumption of using a smaller version of the dataset with 20k images. 

The model suffered with overfitting, evident through sudden increase of validation loss to 28.82 in 9th epoch. As expected, the model performed very well on test images with 98% accuracy and failed tremendously with unseen Amazon images classifying all pictures for 'Men'.

The two explainations for overfitting, in my opinion were : Small dataset and Model complexity.
For the first reason, there wasn't much I could do. As for second, I tried to simplify the model complexity but the model accuracy suffered only more.

The logical explaination at the time seemed - the process of feature extraction in my code is inefficient and transfer learning might be the rescue which might capture patterns even with only 20k images. 

Later, I tried to implement VGG-16 pre-trained imagenet weights for model training, but this time, the Kaggle notebook ran out of space. At the time while generating image vectors and label vectors through one-hot encoding, the Kaggle RAM of 30 GB depleted since around 15-20 GB was used by image data, 5 GB was reserved by the system and rest was not enough because the picture sizes required for VGG-16 were (224,224) instead of old (80,60) in my network leading to exponential increase in arrays of image vectors and labels.

Thus, this version of the notebook has the code written by me in the first attempt with unsuccessful results because of overfitting. And the TensorFlow model from the notebook is at [**Link**](https://drive.google.com/drive/folders/1jotk0lf_IE9XOYzMa75g0FqBTutLw2FO?usp=sharing).

I sincerely hope that the justifications written above would be considered for the model shortcomings.




