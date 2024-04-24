# Book Recommendation Models
## Project 4 - Group 3

### Objective
Utilize machine learning models to produce book recommendations based on an input of book-title.  

### Data
Link: https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset?select=Ratings.csv

### Cleaning of Dataset
[Books.csv](add link) was 'left' merged with [Ratings.csv](add link) and all ratings of 0 were filled with NaN.  Book-Title column was cleaned by renaming books that had title variations (notebook[book_recommender-sparsity-0.5.ipynb](add link)).  This dataframe was exported as [books_ratings_clean_notfiltered.csv](add link).

### Filtering of Dataset
The books_ratings_clean_notfiltered.csv file was further processed for utilization in two different machine learning models: K-Nearest Neighbors and TensorFlow.  
Code for filtering the dataset is available in file [book_recommender-sparsity-0.5.ipynb](add link).  
The users with less than 15 books purchased, and books with less than 50 purchases were removed from the dataset.  These cutoff points were utilized to achieve a target sparsity of less than 99.5%.  This dataframe was exported to csv as [book_rating_cleandf.csv](add link).

### K-Nearest Neighbors Model
The code of the KNN model is availabe in jupyter notebook file [book_recommender-sparsity-0.5.ipynb](add link).
A dataframe of book_rating_cleandf.csv was converted into a pivot table and then compressed into a sparse row matrix with SciPy. This matrix was found to have a sparsity of 99.5%.  
A Scikit-learn K-Nearest Neighbors model was intitiated with a cosine measurement metric and brute algorithm.  The recommender model returns 5 book recommendations and 5 author recommendations.  The author recommendations are based on the return of nearest neighbor books.  The recommender model output was tested by querying the original dataset.  Heatmaps were constructed that visualize how individual users rate the recommended books.  Assessment users were selected based on a high rating of the model input book and their total number of ratings in the dataset.  The KNN model assessment revealed fairly accurate prediction of book satisfaction for a number of users.  

## Requirements
### Data Model Implementation (25 points)
- A Python script initializes, trains, and evaluates a model (10 points)
- The data is cleaned, normalized, and standardized prior to modeling (5 points)
- The model utilizes data retrieved from SQL or Spark (5 points)
- The model demonstrates meaningful predictive power at least 75% classification accuracy or 0.80 R-squared. (5 points)
### Data Model Optimization (25 points)
- The model optimization and evaluation process showing iterative changes made to the model and the resulting changes in model performance is documented in either a CSV/Excel table or in the Python script itself (15 points)
- Overall model performance is printed or displayed at the end of the script (10 points)
### GitHub Documentation (25 points)
- GitHub repository is free of unnecessary files and folders and has an appropriate .gitignore in use (10 points)
- The README is customized as a polished presentation of the content of the project (15 points)
### Group Presentation (25 points)
- All group members speak during the presentation. (5 points)
- Content, transitions, and conclusions flow smoothly within any time restrictions. (5 points)
- The content is relevant to the project. (10 points)
- The presentation maintains audience interest. (5 points)
