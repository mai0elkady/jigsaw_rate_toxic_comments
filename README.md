# jigsaw_rate_toxic_comments
##Project statement and Motivation: Given comments in text format, rate the severity of the toxicity of the comment. The final task is to give scores to pairs of comments such that the one annotated to be more toxic gets a higher score and the one annotated to be less toxic gets a lower score.

## Libraries:
- matplotlib==3.2.2
- nltk==3.2.5
- numpy==1.21.5
- pandas==1.3.5
- pickleshare==0.7.5
- scikit-learn==1.0.2
- scipy==1.4.1

## Files: 
- Data_exploration_and_cleaning.ipyb: notebook that contains functions to read, clean and explore data.
- tfidf_and_ridge.ipynb: Notebook that contains the main analysis, training functions and results.
- LICENSE: contains the license

## Data:
Data is available on Kaggle, the datasets I have used are:
- https://www.kaggle.com/c/jigsaw-toxic-severity-rating/data
- https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data
- https://www.kaggle.com/rajkumarl/ruddit-jigsaw-dataset
- https://www.kaggle.com/nkitgupta/jigsaw-regression-based-data

## Summary of results: 
During my training process, I saved the parameters that lead to the highest average validation accuracy (across 3 versions of the dataset) for each dataset. For all 3 datasets the best analyzer was char_wb with an ngram range between 3 and 5, and the regularization parameter for the ridge regressor is what varried from one dataset to another, For jigsaw, it was 1, for Ruddit, it was 0.1 and for alternative jigsaw dataset, it was 10. The average validation accuracy for these 3 datasets respectively was 0.6811, 0.6229 and 0.6732.

## Acknowledgements: 
The competition and datasets were provided by Kaggle. Some of the code was provided from previous examples on Udacity, and I ackwnoldge the help of some public notebooks on Kaggle that helped me write the final version of the code: https://www.kaggle.com/sytuannguyen/overfitting-lb-is-easier-than-solving-the-problem, https://www.kaggle.com/ducanger/private-0-79-simple-ridge-tf-idf, https://www.kaggle.com/chryzal/jigsaw-ensemble-0-864, https://www.kaggle.com/andrej0marinchenko/best-score-0-856-jigsaw-for-beginners
