# Swiggy-Restaurants-Rating-Classification
Rating Classification using Decision Trees and Random Forest Classifier
This Delhi Restaurant Analysis was inspired by Deevanshi Sharma who posted about a web scraping project called, "Swiggy's Top Rated Restaurant in Delhi" she had been working. After going through the dataset, I asked her about the 345 entries that had no ratings. Turns out, they were not rated at all. I wasn't convinced that that meant a zero rating for those.

Light-Bulb Moment!!

I decided to train and test a random forest model using the remaining 455 rows of data and predict the nearly 300 rows (after cleaning and preprocessing) as unseen data.

These were the steps I took:

------------------------------------------------------
- Preprocessing the dataset

Original columns were: Name, Cuisine, Location, Rating, Number of ratings, Price for two.

New columns: Twelve Categorical vars (0/1)- num_indian, juice,pizza, japanese, ice_cream, american, Thai, Italian, chinese, fast_food, desserts_, snacks_, beverages_.
Bakery (NO/YES)

Numeric vars: num_items, price_for_two,  rating, rated

I used one-hot encoding to convert the cuisine list for each restaurant into binary categorical features.

All ratings wer subject to this scale:
Above 4.0 - GOOD
Greater than 2.5 and less than 4.0 -  FAIR
Less than 2.5 - POOR

-----------------------------------------------------

IN JUPYTER NOTEBOOK

- importing libraries sklearn, numpy, etc.

- importing data

- checked for null values, unique values and possible data types that need changing.

- Exploratory data analysis (EDA)
Three insights from that were: Restaurants with more indian cuisines on the menu scored good

- Further splitting of these features using dummy encoding for faster processing and prevent wrongly perceiving the data as continuous.

- Scaling the columns


- Splitting dataset into training and test.

- Fitting the training set to Decision Tree Classifier (with maximum depth eventually set to 5 after tuning it)

- Plotting feature importance chart.

RESULTS

Order of feature importance:
- Number of items
- Price for two
- Number of indian cuisines on menu
- Presence of dessert on menu
- Menu with no fast food
- Menu with pizzas available
- Menu with American cuisines
- No Thai on menu
- Italian cuisines on menu
- Ice Cream available on menu


