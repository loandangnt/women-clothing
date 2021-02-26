# Topic Modeling Customers' Text Reviews on Women Clothings
## *What does customers complain about the product?*
![banner](./ft1.jpg)



## Overview
This project aims to **extract meaning from customer' text reviews** to identify what issues that customers dislike on a particular product. Retailers can use the insights to prioritize improvement on the most frequently complaining issues. The model produces a probability weights coresponding to each buckets of issues for each negative review text (a negative review text in this analysis is defined as low rating lower than 3 in a scale of 5). Out of the **k** buckets of issues extracted from the model, each text will be assigned an issue that have the highest probability weight.

I use topic modeling techniques using Latent Dirichlet Analysis LDA. Ultimately, validating unsupervising model is extreme difficult, especially in the NLP. Current evaluations of topical quality rely heavily on experts eaminations, i.e. human eyes validation involved. Based on human reading and validation, this model achieved 57% accuracy, and 77% accuracy on 90% percentile of probability weight. This performance is due to the model's inability to 'understand' the ironicallity and different style of different customers, and such a narrow subjects of this dataset, making it challenging to avoid topical overlap.

Further improvement areas includes a significant amount of revision: modifying the vocabulary to include acronyms and multi-word phrases, removing nonsensical topics, conducting parameter search, and comparing with other models.

An **interactive version** of the final model is hosted on Heroku. Check it out [here](https://hate-speech-predictor.herokuapp.com/)!

### Business Questions
There are many possible exploratory text analysis, supervised and unsupervised model techiniques on this dataset. Some business questions in scope of this analysis are:

1. Based on review and rating, what do customers like and dislike about a clothing item? Are there any difference between **category** and **department**?
Solutions: Word count TF-IDF, Bag of words, Wordcloud visualization.

2. How to **prioritize which issue for improvement** for a clothing item?
Solution: Topic modeling using LDA on text reviews.

3. How to choose which **PRODUCT** to improve first?
Solution: Rating statistics, LDA output model accuracy (more accurate prediction is prioritized)


### High Level Approach

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
https://nbviewer.jupyter.org/github/loandangnt/women-clothing/blob/master/women_clothing_data_exploration.ipynb





### LDA Topic Modeling
#### Data Pre-processing
#### Modeling
#### Choosing optimal k number of topics
#### Model output visualization
#### Model output evaluation
 
### Apply LDA Model Result
#### *How to choose which product to adress first?*
### Conclusion

### Next Steps
