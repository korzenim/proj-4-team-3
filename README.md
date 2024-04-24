# proj-4-team-3

**Tensorflow Model
This code contains a book recommendation system built using tensorflow.
The model has two layers of input features which are Book Title and User ID and one output feature which is the rating. The model predicts the rating for a book based on the user ID. 
The original dataset is used for training and testing the model. 80% of the data is used for training and 20% for testing.

For the first iteration of the model, 
the three datasets are merged and the columns “Locations”,”Image-URL-S”,”Image-URL-M” and Image-URL-L are dropped
the Book-Title column is scaled using LabelEncoder
maximum number of User IDs and maximum number of Book-Titles are used for the embedded layer vector
three dense layers with 128, 64 and 32 neurons each are used
loss is calculated using mean squared error and optimized using adam optimizer
the model is run for 3 epochs
dropout layers are used in between the dense layers
The dropout layer randomly sets input units to 0 with a frequency of rate at each step during the training to avoid overfitting.
the training data has a loss of 7.6% and the testing data has a loss of 12.6%

The model was optimized using a smaller dataset (dataset_rating_cleandf.csv) by filtering the original dataset. With this configuration, 
Loss in training data is 10.9%.
Loss in testing data is 11.8%.

**Observations

The loss in training data is higher compared to the original dataset.
The loss in testing data is lower compared to the original dataset.
The performance is better in terms of response time for the model prediction (1m 16s for original model and 15s for optimized model.
The recommendations of tensorflow model is different from the recommendations of KNN model.

