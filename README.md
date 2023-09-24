## House_price_linear_regression
# Linear Regression Machine Learning Project for House Price Prediction

# Problem Statement
A real state agents want the help to predict the house price for regions in the USA. He gave you the dataset to work on and you decided to use Linear Regressioon Model. Create a model which will help him to estimate of what the house would sell for.

## Dataset 
  it contains 7 columns and 5000 rows with CSV extension. The data contains the following columns :

'Avg. Area Income': Avg. Income of householder of the city house is located in.

'Avg. Area House Age': Avg. Age of Houses in same city.

'Avg. Area Number of Rooms': Avg. Number of Rooms for Houses in same city.

'Avg. Area Number of Bedrooms': Avg. Number of Bedrooms for Houses in same city.

'Area Population': Population of city.

'Price': Price that the house sold at.

'Address': Address of the houses.

## Importing Libraries
In this project, we imported the necessary Python libraries, including pandas, numpy, seaborn, and matplotlib, to help us with data manipulation, visualization, and analysis.

## Importing and Exploring Data
We loaded our dataset from a CSV file named 'USA_Housing.csv' into a Pandas DataFrame called `data`. We checked the first few rows of the dataset using `data.head()` to get a glimpse of its structure. The dataset contains information on various attributes such as income, house age, number of rooms, and population, among others.

We performed initial data exploration using `data.info()` to understand the data types and check for missing values. Fortunately, there were no missing values in the dataset.

To gain further insights, we utilized `data.describe()` to obtain statistical summary information about the numerical features in the dataset. This summary included statistics like mean, standard deviation, minimum, maximum, and quartiles for each numerical attribute.

We also examined the column names using `data.columns` to have a clear understanding of the available features.

## Exploratory Data Analysis (EDA)
To visually explore the dataset and understand the relationships between variables, we conducted exploratory data analysis (EDA) using Seaborn. We created a pair plot with `sns.pairplot(data)` to visualize pairwise relationships between numerical attributes. Additionally, we generated a distribution plot using `sns.distplot(data ['Price'])` to visualize the distribution of house prices. Moreover, we used a heatmap (`sns.heatmap()`) to display the correlation matrix among numerical features with annotations.

## Training a Linear Regression Model
In the next phase, we built a Linear Regression model to predict house prices based on the available features. We divided the dataset into training and testing sets using `train_test_split` from Scikit-Learn. We allocated 60% of the data to the training set and 40% to the testing set, ensuring reproducibility by setting a random seed (`random_state=101`).

We created an instance of the Linear Regression model, fitted it to the training data, and evaluated the model's performance.

## Linear Regression Model Evaluation
We evaluated the Linear Regression model by examining key metrics:

- *Intercept:* The intercept of the regression model was approximately -2,640,159.80.

- *Coefficients:* The coefficients for each feature were as follows:
  - Avg. Area Income: 21.53
  - Avg. Area House Age: 164,883.28
  - Avg. Area Number of Rooms: 122,368.68
  - Avg. Area Number of Bedrooms: 2,233.80
  - Area Population: 15.15

## Predictions
We made predictions on the test data using the trained Linear Regression model and created a scatter plot to visualize the predicted prices against the actual prices. The scatter plot showed a linear relationship, indicating that the model made reasonably accurate predictions.

## Regression Evaluation Metrics
To quantify the model's performance, we calculated several regression evaluation metrics:

- *R SQUARE_Score  :* The R Square was approximately 0.9170626478020534, representing the average absolute error between predicted and actual prices.

- *Mean Squared Error (MSE):* The MSE was approximately 10,460,958,907.21, indicating the average squared error.



## Conclusion
In conclusion, this project successfully utilized Linear Regression to predict house prices based on various attributes. The model performed reasonably well, as indicated by the evaluation metrics and visualizations. Further refinement and feature engineering could potentially improve the model's accuracy, but this project serves as a solid foundation for house price prediction using machine learning.
