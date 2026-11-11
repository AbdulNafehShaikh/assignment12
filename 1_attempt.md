the dataset contains information about the prices of different everyday items across the two cities over a period of time. It has 97 rows and 6 columns, including data, item, city, price and unit. Before examining the dataset I will try to identify anything that seems incorrect inconsistent and incomplete.
Problems
Problem 1: Incorrect price format
Code used: df.info() and df["price"].unique()
What I found: The price column is stored as text instead of numerical data. One of the prices is written as “1,250” rather than a regular numerical value.
Planned decision: Correct the format and convert the column into numerical data.
Reason: Prices need to be numerical to perform calculations and compare them properly.

Problem 2: Unusually high price
Code used: df["price"].unique() and df.describe()
What I found: One price is recorded as 9999, which is significantly higher than the other prices in the dataset.
Planned decision: Flag for further investigation.
Reason: It could be a typing mistake or an unusual observation. I would not remove it without checking first.

Problem 3: Incorrect date data type
Code used: df.info()
What I found: The date column is stored as an object (text) instead of a proper date format.
Planned decision: Convert it into a datetime format.
Reason: This would make it easier to arrange the observations by date and analyse price changes over time.
