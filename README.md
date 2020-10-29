# Seattle-home-price-model

# Predicting home prices in King County

# Scenario: 
## I am a real estate developer, in Seattle, looking to see what home feutures and factors should I focus on when investing in real estate in the area.

# Process & Tools Used:
## kc_house_data.csv (file provided)

# Initial findings 
## I started with three question:
### Q1: How significant is location on price?
### Q2: Is outdoor space i.e. squarefootage in the 'lot' that is not accupied by the house, usefull?
### Q3: Does the neighborhood a house is in matter?

## Q1:
grapgh
graph
grpah
graph
## A1: Homes of all values seem to be spread arount with no particular long or lat being a good predictor for price. Simmilarly, while zipcode is a poor predictor of price, most of the more expensize homes are concentrated in a few zipcodes.

## Q2:
graph usage
### Home price and Usage (a home's sqft/lot size) havea correlation coeficcient of 0.2
## A2: The size of a home relative to the size of it's lot does not appear to have a signifigant effect on price.

## Q3:
corr
corr
graph
graph
## A home's neighborhood i.e. 15 closest houses looks to be a reasonable predictor of said hom'es sqft, however, it holds a more limmited abilty to predict lot size. Additionally, and more significantly, neighther appear to be good predictors of price.   

# Model
### An initial model with only the initial built in variables has a testing MSE of 44,553,462,124.30715 and an R^2 or 0.669
OLS graph
### Adding in dummy variable brings the test MSE down to 25,033,004,505.2455 and bring the R^2 up to 0.816
### I added age (the year a homes was sold minus the year it was built) and usage (what percent of a home's lot is taken up by the home). This brings downt the test MSE to 24,850,711,454.54593 but also brings down the R^2 to 0.811
### Next, I got rid of bedrooms since it had a negative coeficient and replaced it with a bed/bath ratio. This brought the MSE back up to 26,466,816,784,675.883 and the the R^2 back up to 0.816
### After an iterative process of dropping variable with high P-values and badly fitting variables I settled on a final model with a test MSE of 24,585,700,133.95531 and an R^2 of 0.813
ols graph

# Conclusions
## With an R^2 over 0.8 and an RMSE under $160,000 my model appears to do a reasonable job at predicting the effect of certain homes feutures. 
### From my initial analysis it appears that a home's specific location is less relavent than it's neighborhood. The model also help to support this idea via different coeficcients for different zipcodes.
### As a 'investor' if I am looking for existing homes I should highly value waterfront homes. And if I am adding on to or building a home above ground sqft or more valuable than basement sqft by over 50%.
### Finally, given the model's error size it is worth taking the above conclusions with a grain of salt.

# Future Work
## Variables
### Getting data on additional home feutures, as well as, looking at how time affects it all would likely yield more acurate outcomes.
## Model
### It seems posible that all, or at least some of the data could be better analyzed using non-linear methods


 

















