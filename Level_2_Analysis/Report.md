# Amazon Review Analysis - are Vine Reviews trustworthy?

The goal of the Amazon Review Analysis was to find out wether the Vine reviews are truly trustworthy or not. <br>
I took "Electronics" (over 3M rows) & "Kitchen" (almost 5M) datasets from [Amazon review list](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt). After extracting and transforming data, I selected the relevant columns for my analysis, these are `review_id`, `star_rating`, `helpful_votes`, `total_votes`, and `vine`. Then, I split the reviews between Vine (paid) and non-Vine (unpaid) and compared metrics between them. I looked at number of total reviews, number of 5-stars and 1-star, average ratings, standard deviation, and number of helpful votes. <br>

---

## Summary of finding from the "Electronics" and "Kitchen" datasets <br>

**Electronics - 3,093,861 total reviews**<br>

Total percentage (number) of reviews: <br>
Vine: </t>          0.6% (18,512) <br>
Non-Vine:       99.4% (3,075,349) <br>

Percentage of 5-star reviews (number):<br>    
Vine:           43% (8,044)<br>
Non-Vine:       57% (1,773,112)<br>

Percentage of 1-star reviews (number):<br>    
Vine:           1.8% (342)<br>
Non-Vine:       11.6% (357,777) <br>

Average rating (1-5):<br>
Vine:           4.13 <br>
Non-Vine        4.03 <br>

Standard deviation: <br>
Vine:           0.96 <br><br>
Non-Vine        1.39 <br>

Average number of helpful votes (per review): <br>
Vine:           5.82 <br>
Non-Vine:       1.83 <br>

Percentage (number) helpful votes (per review): <br>
Vine:           61% (11,367) <br>
Non-Vine:       32% (991,372) <br>
<br>
<br>

**Kitchen - 4,880,460 total reviews** <br>
Total percentage (number) of reviews: <br>
Vine:           0.5% (24,434) <br>
Non-Vine:       99.5% (4,856,026) <br>

Percentage of 5-star reviews (number): <br>   
Vine:           48% (11,753) <br>
Non-Vine:       64% (3,116,807) <br>

Percentage of 1-star reviews (number):<br>    
Vine:           1.4% (351)<br>
Non-Vine:       8.8% (426,954) <br>

Average rating (1-5):<br>
Vine:           4.24<br>
Non-Vine        4.21 <br>

Standard deviation:<br>
Vine:           0.89<br>
Non-Vine        1.28 <br>

Average number of helpful votes (per review):<br>
Vine:           5.96<br>
Non-Vine:       2.23 <br>

Percentage (number) helpful votes (per review):<br>
Vine:           53% (12,965)<br>
Non-Vine:       34% (1,690,670) <br>

---

**Impact of paid reviews** <br>
The number of Vine reviews in both datasets is negligible (less than 1%) compared to total number of reviews. The paid reviews (Vine program) won't influence purchasing decisions at a big scale.  <br>

**The best and the worst: 5-star and 1-star rated reviews** <br>
5-star reviews show surprising results. It would be expected to have higher percentage of paid 5-star reviews compared to unpaid. In both datasets, paid 5-start reviews are below 50%, and unpaid are around 60%. These numbers are telling us that paid reviewers are not necessarily biased even though they get money for their service. The absolute percentage of people writing good reviews is pretty high, which means that they provide positive feedback if they like the product no matter if they're getting paid or not.
1-star reviews highlight the fact that unpaid reviewers have less of a filter than paid ones when it comes to negative feedback. Percentage-wise, there are about six times more 1-star unpaid reviews than paid. <br>

**Average rating** <br>
The average rating difference for Vine and non-Vine reviews is very minimal (less than 0.1 in the average rating gap). This shows that Vine reviews can be trusted as these reviewers stay objective and are not influenced by the fact they are paid. <br>

**Analysis of reviews which we marked as helpful** <br>
The percentage of reviews classified as helpful is substantially higher for Vine reviewers. Almost twice as many reviews are being helpful for Vine (53% in Kitchen dataset, 61% in Electronics dataset) compared to non-Vine (34%, 32% respectively). Average number of helpful feedback is also much higher for Vine reviews (5.96 in Kitchen dataset, 5.82 in Electronics dataset) compared to non-Vine (2.23, 1.39 respectively). This shows that paid reviews are written more constructively. <br>

**Does the data form different datasets telling us the same story?** <br>
The short answer is yes. If you look at the above summary metrics, you can see that the numbers (percentage and averages) are very similar. Behavior is also similar. <br>

### Conclusion <br>
Vine reviews are trustworthy and in addition, these reviews are more constructive than non-paid as people who get paid put more thought to their reviews. It may be helpful to the consumer to have more of these paid reviews.