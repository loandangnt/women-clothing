# Analyze e-commerce customers' reviews on women clothings
Data:

- The entire analysis answers these questions:
Questions	Can be answered or not?	How?
1. Based on review and rating, what customers like and don't like about clothing by category, department?	yes	Clustering, wordcloud, visualization (count frequent words, polarized tag plot (compare word frequency bet. positive review (>3) and negative (<3), will be good if I can do it interactively)?
2. Is the rating consistent with review?	yes	Rating is consistent with review and Rec IND
3. How do we prioritize issues about each clothing category (topic modeling)?	yes	Topic modeling with LDA
4. Can we use this data to predict if a review is negative or positive? How to see if a product is being reviewed negative or positive and how to predict if a product would be liked or disliked?		Classification model (use rating or recommendation as label)
5. If you are the one who is in charged to address very serious issues exist with most products/ some segment of products in the website, how do you use this data to address it?	yes	I would find a pattern that gives me sign of particular bad feature of product. Then, I will filter out the existing bad reviewed products, which are categorized into bucket of problem type. Second, I will use these patterns to predict if a particular product, receiving similar initial review, would continue to be disliked so that Customer Service/ Product team can be involved in soon.
6. Explore data to find pattern/insight: word association (clustering)	yes	size/small is the most prominant problem among bad reviews
Opinion of Group of customer (Age, Title) towards different cloth categories (younger customer is more picky? they tend to buy more 'Trendy' cloth? that may be why trendy cloth has more bad reviews??		

- LDA Topic Modeling:
Problem statement: I'm trying to see what people complained about a product. Retailers can use the insights to prioritize improvement on the most frequently complained issues. The model segments negative review texts (low rating average, <3), and will give us an idea of what customers complain about the product on a review/purchase. I use topic modeling technique - LDA model. An expected result of the model would be that, for clothing id 1001, a negative review complained mostly about material.

Model output assessment: Human observations, Wordcound visualization.

Delivery: Each low rated Clothing Category receives top 3 prioritized areas of improvement for their product and service.
 
