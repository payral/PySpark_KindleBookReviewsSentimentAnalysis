# PySpark_KindleBookReviewsSentimentAnalysis
Using Pyspark and Pandas to do EDA and predictions for positive and negative reviews on Kindle Books. Working with Big Data.

## File Descriptons

**kindle_reviews.csv**: Dataset for the project. Originally 680 MB, reduced to upload to github

**amazon_reviews_eda.ipynb**: Exploratory data analysis for the project. Includes removing stop words, wordclouds, and a word2vec

**amazon_reviews_modeling.ipynb**: The machine learning is in PySpark for this project. I also used linear and logistic regression, random forest, as well as naive bayes. The project was done using databricks, so when viewing the pipelines and machine learning for this file, you have to scroll down very far to see the code before and after the display() methods. Use _Ctrl+F VectorAssembler_ to avoid this.

## Pipelines

For the pipeline I used HashingTF, StringIndexer, OneHotEncoder, finalized by VectorAssembler.

## Results

Each of the algorithms produced good results. They were each able to get above 90% accuracy, with Naive Bayes doing the best, with a test accuracy of 96.4%.

## Future Work

The purpose of sentiment analysis is to find the negative reviews and address them. Therefore, I realized that false negatives were not as much of a concern as false positives: its okay to have some positive reviews be counted as negatives, but its bad if a negative review is seen as positive. In the future, I would want account for this and fine-tune my model. 
