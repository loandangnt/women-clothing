# Analyze e-commerce customers' reviews on women clothings
This is a Kaggle dataset. Link: https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews:
"Context

Welcome. This is a Women’s Clothing E-Commerce dataset revolving around the reviews written by customers. Its nine supportive features offer a great environment to parse out the text through its multiple dimensions. Because this is real commercial data, it has been anonymized, and references to the company in the review text and body have been replaced with “retailer”.

Content

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
Class Name: Categorical name of the product class name."

- Business questions for this dataset:
Questions	Can be answered or not?	How?
1. Based on review and rating, what customers like and don't like about clothing by category, department?	Yes	Clustering, wordcloud, visualization (count frequent words, polarized tag plot (compare word frequency bet. positive review (>3) and negative (<3), will be good if I can do it interactively)?
2. Is the rating consistent with review?	Yes	Rating data is consistent with review and Rec IND.
3. How do we prioritize problems for improvement area for each clothing item/category (topic modeling)?	Yes	Topic modeling using LDA
4. Can we use this data to predict if a review is negative or positive? How to see if a product is being reviewed negative or positive and how to predict if a product would be liked or disliked?		Not in scope Classification model (use rating or recommendation as label)
5. If you are the one who is in charged to address very serious issues exist with most products/ some segment of products in the website, how do you use this data to address it?	Yes	I will find the most problematic Clothing items. Then, I will identify which are the most prominant problems with these products (sovled by LDA topic modeling task in wuesation 3 above).

- LDA Topic Modeling:
1. Problem statement: I'm trying to see what people complained about a product. Retailers can use the insights to prioritize improvement on the most frequently complained issues. The model segments negative review texts (low rating average, <3), and will give us an idea of what customers complain about the product on a review/purchase. I use topic modeling technique - LDA model. An expected result of the model would be that, for clothing id 1001, a negative review complained mostly about material.
2. Model output assessment: Human observations, Wordcound visualization.
3. Delivery: Each low rated Clothing Category receives top 3 prioritized areas of improvement for their product and service.
 
