- Histogram of house price distribution - shows the overall distribution of house prices
- Box plot of house price and number of bedrooms - analyzes the range of house prices corresponding to different numbers of bedrooms
- Box plot of prices of different property types - compares the price distribution of various property types
- Histogram of BER rating and house price - shows the correlation between energy rating and house price
- Heat map of geographical distribution of house prices - visualizes the geographical distribution of house prices by latitude and longitude
- Heat map of feature correlation - analyzes the correlation between various numerical features

It mainly implements the training and evaluation functions of the house price prediction model. The code retains key feature columns including the number of bedrooms, number of bathrooms, latitude and longitude, property type, BER energy efficiency rating and country.
In order to improve accuracy, the code implements a number of improvements:
1) Data preprocessing including handling missing values ​​and outliers
2) Added derived features such as estimated area and distance to center
3) BER ratings were numerically mapped
4) Logarithmic transformation was used to process prices
5) Three different models (SVM, random forest, KNN) were implemented and performance was compared, among which the random forest model performed best and was selected as the final model



Data processing: merge_datasets.py is responsible for merging three real estate data sets from different sources (daft_housing_data.csv, uae_properties.csv and zp1.csv), unifying the column names and data formats.
Model training: price_prediction.py implements the house price prediction model, retaining key features such as the number of bedrooms, the number of bathrooms, longitude and latitude. Through data preprocessing, feature engineering and model optimization, the best performing random forest model was finally selected.
Visualization display: It includes multiple charts such as house price distribution, average price of property type, average price of BER rating, feature correlation, etc., to help understand data characteristics and model performance.
Web application: The web interface is built through the Flask framework. Users can enter real estate information to obtain predicted prices, and various data visualization charts are displayed through ECharts.