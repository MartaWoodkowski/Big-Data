# Big Data - Analysis of Amazon's Vine Program Reviews 

Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. However, they are quite large and can exceed the capacity of local machines to handle. Smallest dataset contains over 1.5 million rows; with over 40 datasets, this can be quite taxing on the average local computer. 

Performed ETL process in the Cloud and uploaded a DataFrame to an RDS instance. Then, used PySpark and Spark SQL to perform a statistical analysis of selected data. Created DataFrames to match production-ready tables from two big Amazon customer review datasets. Analyzed whether reviews from Amazon's Vine program are trustworthy.

- - -
### Level 1 - ETL

* Used the furnished schema to create tables in the RDS database.

* Created two separate Google Colab notebooks (due to large size of data) and **extracted** "Electronics" (over 3M rows) & "Kitchen" (almost 5M) datasets from the list at [review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), one into each notebook.

* **Transformed** the dataset to fit the tables in the [schema file](../Resources/schema.sql).

* **Loaded** the DataFrames that correspond to tables into an RDS instance.

### Level 2 - Analysis of Amazon Reviews

In Amazon's Vine program, reviewers receive free products in exchange for reviews.

  ![vine01.png](../Images/vine01.png)

Amazon got several policies to reduce the bias of its Vine reviews: [https://www.amazon.com/gp/vine/help?ie=UTF8](https://www.amazon.com/gp/vine/help?ie=UTF8).
But are Vine reviews truly trustworthy? I investigated whether Vine reviews were free of bias. 

* Performed the analysis in Cloud using Python and Spark (on Google Colab).

* Reduced noisy data, e.g., filtering for reviews that meet a certain number of helpful votes, total votes, etc. Performed summary statistics and more.

* Written report of my findings you can find [here](Level_2_Analysis/Report.md).

- - -
### References

Amazon customer Reviews Dataset. Retrieved from: [https://s3.amazonaws.com/amazon-reviews-pds/readme.html](https://s3.amazonaws.com/amazon-reviews-pds/readme.html)