# Analyze e-commerce customers' reviews on women clothings
This is a Kaggle dataset. Link: https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews:

This is a Women’s Clothing E-Commerce dataset revolving around the reviews written by customers. Its nine supportive features offer a great environment to parse out the text through its multiple dimensions. Because this is real commercial data, it has been anonymized, and references to the company in the review text and body have been replaced with “retailer”.

This dataset includes 23486 rows and 10 feature variables. Each row corresponds to a customer review, and includes the variables:

Clothing ID: Integer Categorical variable that refers to the specific piece being reviewed.
Age: Positive Integer variable of the reviewers age.
Title: String variable for the title of the review.
Review Text: String variable for the review body.
Rating: Positive Ordinal Integer variable for the product score granted by the customer from 1 Worst, to 5 Best.
Recommended IND: Binary variable stating where the customer recommends the product where 1 is recommended, 0 is not recommended.
Positive Feedback Count: Positive Integer documenting the number of other customers who found this review positive.
Division Name: Categorical name of the product high level division.
Department Name: Categorical name of the product department name.
Class Name: Categorical name of the product class name.

- Business questions for this dataset:

1. Based on review and rating, what customers like and don't like about clothing by category, department?	Wordcloud, visualization

2. How to prioritize problems for improvement area for a clothing item/category?	Topic modeling using LDA

3. How to choose which product to be treated/improved first? Rating statistics; LDA output model accuracy (more accurate prediction is prioritized)

- LDA Topic Modeling:
1. Problem statement: I'm trying to see what people complained about a garment item. Retailers can use the insights to prioritize improvement on the most frequently complained issues. The model segments negative review texts (low rating average, <3), and provides information about what customers complain about the reviewed item. I use topic modeling technique - LDA model.
2. Model output evalution: Human observations, Wordcloud visualization.
3. Delivery: An expected result of the model would be that, for clothing id 1001, a negative review complained mostly about material. Each low rated Clothing Category receives top 3 prioritized areas of improvement for their product and service.
 
