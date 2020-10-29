# Seattle-home-price-model

# Predicting home prices in King County

# Scenario: 
I am a real estate developer, in Seattle, looking to see what home feutures, if added, are likely to increase a homes value.

# Process & Tools Used:
## kc_house_data.csv (file provided)








RangeIndex: 21597 entries, 0 to 21596
Data columns (total 21 columns):
 #   Column         Non-Null Count  Dtype  
---  ------         --------------  -----  
 0   id             21597 non-null  int64  
 1   date           21597 non-null  object 
 2   price          21597 non-null  float64
 3   bedrooms       21597 non-null  int64  
 4   bathrooms      21597 non-null  float64
 5   sqft_living    21597 non-null  int64  
 6   sqft_lot       21597 non-null  int64  
 7   floors         21597 non-null  float64
 8   waterfront     19221 non-null  float64
 9   view           21534 non-null  float64
 10  condition      21597 non-null  int64  
 11  grade          21597 non-null  int64  
 12  sqft_above     21597 non-null  int64  
 13  sqft_basement  21597 non-null  object 
 14  yr_built       21597 non-null  int64  
 15  yr_renovated   17755 non-null  float64
 16  zipcode        21597 non-null  int64  
 17  lat            21597 non-null  float64
 18  long           21597 non-null  float64
 19  sqft_living15  21597 non-null  int64  
 20  sqft_lot15     21597 non-null  int64  
dtypes: float64(8), int64(11), object(2)

An intitial look at the data shows the need to clean/edit it.

After removing removing erroneous variables converting all data to numeric form I moved onto dealling with missing data. With a largenough data set and minimal missing data I opted to drop rows containing missing and null values.

Next I looked to drop outlier data points:
data=data[data['sqft_living']<12000]
data=data[data['sqft_lot']<1500000]
data=data[data['sqft_above']<8000]
data=data[data['sqft_basement']<4000]
data=data[data['sqft_lot15']<800000]

Moving onto the problem of collinearity I inspected the date