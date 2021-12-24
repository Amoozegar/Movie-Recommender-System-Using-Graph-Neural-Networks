# Movie Recommender System via Graph Neural Network
### Deep Learning Final Project - Team: AI Pioneers

This respository provides python code, google co-lab notebooks, graphs and outputs for the application of Graph Neural Networks for Recommender Systems. It contains three Google Colab notebooks
- data-eng.ipynb
    *  Clean the data
    *  Extract the desired information
-  DL-Final-Project.ipynb
    * Train a Graph Neural Network model to recommend movies to users.
    * Inference for all users
- Hyper-Parameter-Tune.ipynb
    * Parameter tuning

The Graph Neural Network in this project is is written in Python3 and implemented based on the DGL (Deep Graph Library [DGL](https://docs.dgl.ai/)).


## **Dataset**
This project focuses on implementing a recommender system for movies using MovieLense 1M dataset. This dataset includes three sets of data which contain 1,000,209 anonymous ratings of approximately 3,900 movies made by 6,040 MovieLens users who joined MovieLens in 2000:
  - movies.dat
  - ratings.dat
  - users.dat


### Users
User information includes the following features:

    Users -->  ['UserID', 'Gender', 'Age', 'Occupation', 'Zip-code']

However, for this project, we only considered the Gender as an attribute for users and removed all other features.

     Users --> ['UserID', 'Gender']

### Movies

    Movies --> ['MovieID', 'Title', 'Genres']


### Ratings (Users-Movies Interactions):

    interacts_df --> ['UserID', 'MovieID', 'Rating', 'Timestamp']


## **GNN**

### Training
Model Training, validation and inference is done using DL-Final-Project.ipynb notebook. It includes all the classes and methods required for GNN.


### Inference
With a trained model, it is possible to generate recommendations for all users or specific users. DL-Final-Project.ipynb notebook provide the code for inference as well.


### Hyper Parameters Tuning
We need to select the hyperparameters, and the run the cell to train, test and validate the GNN model. It will report the metrics for each model. The Hyper-Parameter-Tune notebook only receives the parameters as the input and calls the tuning_model.py scrupt.


### Outputs & Plots
Plots of the training experiments are saved in the plots directory.
