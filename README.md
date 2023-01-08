# SparkSQL-EMR

### Goal:
Use Spark on EMR cluster to manipulate the datasets about Amazon products and their reviews. 

eg.
Analysis in sdf:

- find the average rating for products based on category

- find the percentage change from 2010 to 2011 in both average overall rating and average price for products based on category

- When you navigate to the Amazon webpage, you are often recommended some bestsellers. These bestsellers are recommended to you based on several factors, one of them being positive ratings and reviews. Most popular products have tons of reviews and ratings from customers. We're going to look into popular products bought in a few categories to dive deeper into the consumer market culture.

- find the 5 most commonly reviewed products around Christmas in the Toys and Games category.

- We are interested in finding the products that are most frequently reviewed within the Home and Kitchen category. 
- Find the top three months in which products from the Home and Kitchen category are most frequently reviewed during the years 2010 to 2014 (inclusive).

- You don't always have time to read an entire review. When you're about to buy a product you love, you may scroll through some reviews, eyeballing the summaries and how helpful the reviews are. Eyeballing a few reviews that comment on the usability of the product like "cheap but works" or "effective" or "waste of money" can help you make your decision. Your task is to count the number of reviews per category where the summary length is less than 10 characters and it is considered useful.

- Find how helpful a review is in terms of a ratio, and return the top 10 most helpful reviews, the corresponding reviewerID and the helpfulness ratio. 


Mastering SQL is more beneficial than being able to use Spark commands (functions) as it will show up in more areas of programming and data science/analytics than just Spark.

### Techniques:
Spark, SparkSQL, EMR, Spark dataframes (sdf), schema design, JSON

### Datasets:

Data is stored in an AWS S3 bucket, so I would download it onto the nodes of my EMR cluster.

There are 3 JSON datasets with information about the products and 3 JSON datasets with information about the customer reviews for these products. The three categories of products are: 

1. Gourmet & Grocery Food
2. Toys & Games
3. Home & Kitchen


### Challenges:
When loading data, Spark will try to infer its structure on its own. This process is faulty because Spark will sometimes infer the type incorrectly. Spark's ability to determine types is not reliable, thus you will need to define a schema for [] and .

----------------
如果要写简历的话:

1. ingest datasets from S3 bucket to Spark dataframe on EMR
2. Design schema from structure type for JSON object on Spark
3. Cleaned Spark dataframe in SparkSQL by aggregation and division based on certain schema, formats and orders that fit on business targets.
4. optimized SparkSQL query to analyze metrics and discover business insights
