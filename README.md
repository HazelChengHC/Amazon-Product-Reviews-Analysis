# SparkSQL-EMR

### Goal:
Use Spark on EMR cluster to manipulate the datasets about Amazon products and their reviews. 

Mastering SQL is more beneficial than being able to use Spark commands (functions) as it will show up in more areas of programming and data science/analytics than just Spark.

### Techniques:
Spark, SparkSQL, EMR, Spark dataframes (sdf), schema design, JSON

### Datasets:

Data is stored in an AWS S3 bucket, so I would download it onto the nodes of my EMR cluster.

There are 3 JSON datasets with information about the products and 3 JSON datasets with information about the customer reviews for these products. The three categories of products are: 

1. Gourmet & Grocery Food
2. Toys & Games
3. Home & Kitchen
