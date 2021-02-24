# Topic Modeling Customers' Text Reviews on Women Clothings
## *What does customers complain about the product?*
![banner](./ft1.jpg)

## Overview
This project aims to **extract meaning from customer' text reviews** to identify what issues that customers' dislike on a particular product. Retailers can use the insights to prioritize improvement on the most frequently complained issues. The model segments negative review texts (low rating average, <3), and will give us an idea of what customers complain about the product on a review/purchase.

I use topic modeling techniques using Latent Dirichlet Analysis LDA. Ultimately, verifying unsupervising model is extreme difficult, especially in the NLP area. Current evaluation of topical quality rely heavily experts eaminations, i.e. human eyes validation involved. Based on human reading and validation, this model achieved 77% accuracy. This performance is due to the model's inability to 'understand' the ironicallity and different style of different customers, and such a narrow subjects of this dataset, making it challenging to avoid topical overlap.

Further improvement areas includes a significant amount of revision: modifying the vocabulary to include acronyms and multi-word phrases, removing nonsensical topics, conducting parameter search, and comparing with other models.

An **interactive version** of the final model is hosted on Heroku. Check it out [here](https://hate-speech-predictor.herokuapp.com/)!

### Business Questions

1. Based on review and rating, what do customers like and dislike about clothing **BY CATEGORY, BY DEPARTMENT**?
Solutions: EDA using Wordcloud, visualization, statistics

2. How to prioritize which **PROBLEM** to improve for each clothing product?
Solution: Topic modeling using LDA

3. How to choose which **PRODUCT** to improve first?
Solution: Rating statistics, LDA output model accuracy (more accurate prediction is prioritized)

### Data Sourcing
This is a Kaggle dataset. Link: https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews:
Its nine supportive features offer a great environment to parse out the text through its multiple dimensions. Because this is real commercial data, it has been anonymized, and references to the company in the review text and body have been replaced with “retailer”.

This dataset includes 23486 rows and 10 feature variables. Each row corresponds to a customer review, and includes the variables:
 Column Name | Description |
|-|-|
|1. Clothing ID| Integer Categorical variable that refers to the specific piece being reviewed.
|2. Age| Positive Integer variable of the reviewers age.
|3. Title| String variable for the title of the review.
|4. Review Text| String variable for the review body.
|5. Rating| Positive Ordinal Integer variable for the product score granted by the customer from 1 Worst, to 5 Best.
|6. Recommended IND| Binary variable stating where the customer recommends the product where 1 is recommended, 0 is not recommended.
|7. Positive Feedback Count| Positive Integer documenting the number of other customers who found this review positive.
|8. Division Name| Categorical name of the product high level division.
|9. Department Name| Categorical name of the product department name.
|10. Class Name| Categorical name of the product class name.

### Data Understanding

![](./rating_stats_by_class_dept.html)




### LDA Topic Modeling
#
 
### Apply LDA Model Result

### Conclusion

### Next Steps
