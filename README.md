# Booking Cancellation Analysis
(Data Cleaning, Analysis, Visualization, Feature Selection, Predictive Modeling)
### Problem Statement
The revenue team of a well-known hotel group recently faced a significant problem — an increase in cancellations. This trend not only disrupted the efficient functioning of the hotels but also resulted in substantial revenue losses. The team required insights and solutions: What were the factors driving these cancellations? Were there any identifiable patterns or trends? In order to tackle these crucial inquiries, data analysis emerged as the most powerful tool.

### Task
Our task was clear: to analyze extensive hotel booking data spanning three years, encompassing the years 2018, 2019, and 2020. By meticulously examining this data, we aimed to uncover the underlying causes of hotel cancellations and gain a deeper understanding of the cancellation landscape. Our journey began with data preprocessing, cleaning, and consolidation, to ensure that the dataset was ready for analysis. This included addressing missing values and integrating data from different sources to create a comprehensive dataset.

### Methodology
Our approach was comprehensive, intended to unveil the intricate dynamics of hotel cancellations and provide actionable insights for revenue optimization. This section presents an overview of how we conducted our analysis:

1. Data Preparation: At first dataset, was collected from Github where three years of booking data 2018, 2019, and 2020 can be found. Then data cleansing, handling missing values and discrepancies, merging booking data column and important column to the main dataframe was done. This was important to ensure the accurate analysis for data and predictive modeling to predict the variable accurately.

2. Granular-Level Analysis: We acknowledged that a superficial examination would be inadequate. To acquire a profound comprehension of cancellations, we dissected various factors, including lead time, alterations in room type, modifications in bookings, special solicitations, and customer categories. By delving into the contribution of each of these elements to cancellations, our aim was to furnish the revenue team with actionable insights.

3. Predictive Modeling: The zenith of our analysis encompassed predictive modeling, wherein we harnessed the potential of machine learning. We opted for the Random Forest model, a robust ensemble method, to ascertain the features exerting the most significant influence on cancellations. This empowered us to pinpoint the underlying forces behind cancellations, offering a perspective driven by data that could be leveraged to mitigate cancellations and optimize revenue.

**Random Forest Model:** I selected the Random Forest Classifier as the predictive model. It’s robust, handles both categorical and numerical data well, and provides feature importance scores.

**Feature Selection:** a subset of features found in EDA and I used intuitions, to select features. These features used for modeling are ‘arrival_date_month’, ‘country’, ‘market_segment’, ‘distribution_channel’, ‘reserved_room_type’, ‘deposit_type’, and ‘customer_type’.

**Categorical Data Encoding:** To prepare the categorical features for modeling, you performed label encoding. This process converted categorical values into numerical representations. Label encoding enabled the model to work with these features effectively. Training-Testing Split: Divided the dataset into training and testing sets. Model Training: Fitted the Random Forest Classifier to the training data. The model learned patterns and relationships within the data to make predictions about future cancellations.

**Evaluation and Prediction:** I made predictions on the testing dataset using the trained model. Evaluating the model performed by comparing the results of useful metrics such as accuracy, precision, recall, and F1 score.

**Feature Importance Analysis:** I obtained feature importance scores following model training. The features that most significantly affected the model’s predictions were identified with the use of this investigation.

Random Forest Classifier achieved an accuracy of approximately **78.34%** which I feel is good in the context of analysis.

### Result:
Lead Time (52.70%): This feature holds the highest importance in predicting cancellations. It suggests that the amount of time between booking and the actual stay date plays a significant role. Guests who book well in advance might have different cancellation behaviors compared to last-minute bookers.

Country (18.95%): The origin of the guests, represented by the country variable, is the second most influential factor. Different countries might exhibit distinct booking and cancellation patterns.

Arrival Date Month (9.59%): The month of the year when guests arrive is also a critical feature. Seasonal variations and events might impact cancellation rates.

Market Segment (6.90%): The market segment from which the booking originates holds substantial importance. Different segments (e.g., corporate, groups, and individual travelers) may have varying cancellation tendencies.

Reserved Room Type (4.68%): The type of room reserved is a key factor. Guests booking specific room types may be more or less likely to cancel.

Customer Type (3.05%): The customer type (e.g., transient, group, etc.) is a valuable feature. Different customer segments may exhibit different cancellation behavior.

Deposit Type (2.67%): The type of deposit made during booking is also a significant predictor.

Distribution Channel (1.45%): Cancellations are also influenced by the channel used to make the reservation (e.g., direct reservations, online travel agencies).
