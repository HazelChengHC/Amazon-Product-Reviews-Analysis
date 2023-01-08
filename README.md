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

- We would like to determine the sentiment of some of the reviews across the categories. Sentiment Analysis is used with textual data very regularly. A common application includes determing whether the review associated with a product is positive, negative or neutral. We are going to attempt to determine the sentiment associated with the top 10 most helpful reviews from the food category, based on the ratio calculated in the previous section.

tokenized list of words (removing stop words and checking for alphabets) 从hw2里面参考

Sentiment analysis is a a natural language processing (NLP) technique that attempts to identify the emotional tone behind a body of text. In this case, we will try to determine how posiitve a review is. 

We will be calculating the sentiment associated (系数） with each of these reviews. Sort the df by this column from highest sentiment to lowest.

Now, moving back into SQL, we need you to run a query on the product_reviews_sdf to retrieve the titles of 2 products with the highest sentiment.


--
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
5. tokenize for elementary NLP to do sentiment analysis on customer reviews
