![forsale](https://github.com/lpb3393/Home_Renovations/blob/main/photos/forsale.jpg)





# Business Understanding

This project is to show Century 21 Real Estate that when trying to sell a home, maximizing profit is typically a high priority and rennovations are a key way that to ensure homeowners are getting the most they can from their listing their home. Renovations are important when trying to resell a home for several reasons: 
1. Market demand: The size of a home, as indicated by its square footage, is a key factor that affects market demand. Buyers often have specific space requirements based on their lifestyle and family needs. Renovations that increase the square footage, such as adding an extension or finishing a basement, can expand the home's appeal and attract a wider range of potential buyers.
2. Functional and practical considerations: The number of bathrooms and bedrooms directly impacts a home's functionality and practicality. Buyers typically seek homes with an adequate number of bedrooms to accommodate their family members or provide additional space for guests. Similarly, having an appropriate number of bathrooms is crucial for convenience and privacy. Renovations that add or modify bedrooms and bathrooms can significantly improve the home's functionality, increasing its value and marketability.
The square footage, number of bedrooms, and number of bathrooms are essential criteria used in analysis to determine the value of a home. Appraisers and real estate agents consider these factors when assessing the value of a property and comparing it to similar homes in the area. Renovations that align with these criteria can positively impact the home's appraised value and make it more competitive in the market.


# Data Understanding

This project uses the King County House Sales dataset, which describes homes in the area with attributes such as, price, bedrooms, bathrooms square footage, etc. but not all of these columns are important or influence the price of a house. First I am going to go through the dataset and determine what I find to be most useful and relavent to the analysis. Once I establish what is needed, I will clean up and transform the data to best fit into the OLS model. 


# Data Preparation

After going through the data, I created a new table with just the fields I was interested in and assigned the fields to new variables to easily call back on them when needed. I also used the "describe" and "unique" functions to get a little more information about the data I was working with, like mean, standard deviation, the count, etc. 


# Exploratory Data Analysis

When starting the analysis, I wanted to first see which fields were most strongly correlated to "price" and graph those field to see if they showed a linear relationship. I then created the OLS model several times, trying to increase the R-Squared value each time by adding variables to the model and decreasing the P Value. One way I did that was by creating One Hot Codes for a conditional variable "Condition." This added four new variables to the model and increased the R-Squared value significantly.


# Conclusions

Overall, this model explains about 41% of the variance in price and not all of the variables matter. "Sqft_living" was the most strongly correlated with price and for every increase in one square foot, the value of the home increased by approximately 586 dollars. For "bedrooms", the value decreases by 170,300 dollars for every bedroom added, for evey "bathroom" added the value increases by 135,500 dollars, "sqft_patio" increases value of the house by about 255 dollars. Every year that goes by, according to this  model, the price will decrease by 3,955 dollars and if the condition of the house is "average" the value will increase by 112,800 dollars, "Fair" will increase by 52,460 dollars, "Good" will increase by 82,890 dollars and "Very Good" will increase the most by 116,100 dollars. All values are statistically significant with a P Value less than the standard alpha of 0.05 besides "condition_fair", with has a p-value of 0.588. 


## Limitations

The plot of the residual points of this model showed a p-value much lower than 0.05 (3.32172443457456e-11), which in this case means the opposite, so we reject the null hypothesis and do not consider the relationship to be completely linear. 
There does seem to be a strong correlation between price and some of the variables, though and those that were also statistically sigfinicant are recommendations that I would have for those looking to sell their home.


## Recommendations

If a homeowner is looking to sell their house and is wanting to maximize potential profit, it is important to meet the demands of those looking to buy at that time. The size of the home and the functionality are usually the biggest selling points and if someone can improve upon what they are currently offering, they would typically earn a higher profit. Increasing the livable square footage or adding on a patio are great options, but also potentially adding an additional guest bathroom has shown to increase profit significantly. 


## Next Steps

Adding more interaction variables could be beneficial for the performance of the model. Since the condition of the house had such an impact on the price, it might be interesting to see what kind of effect some environmental factors might have on the price, as they could be pretty significant. Also, possibly including economic information for this region could be very informative because home values have been on such a rollercoster since the pandemic. 



```
├── data
├── images
├── README.md
├── .pdf
└── .ipynb
```
