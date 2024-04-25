# Recommender-System-Using-Neural-Networks


## What is Recommender System, How is it achieved?
Recommender Systems are sophisticated algorithms designed to provide product-revelant-suggestions to users. These systems play a paramount role in enhancing user experience on various online platforms, including streaming services, e-commerce websites, socia media

They achieve this goal by analyzing past user interactions such as ratings, click, purchases. These algorithms can be collaborative (based on user interaction) or content-based (item features). 

## Objective:

The objective of this project is to develop a recommender system using collaborative filtering techniques enhanced with neural networks. The system aims to provide personalized recommendations to users based on their historical interactions with items, such as ratings or clicks. By leveraging neural network architectures, the recommender system seeks to capture complex patterns and relationships in the user-item interaction data, leading to more accurate and effective recommendations.

The process includes 

**Model Development:** Design and implement a collaborative filtering model using neural networks to learn latent representations of users and items from interaction data

**Personalization**: Provide personalized recommendations to users by leveraging the learned user and item embeddings to predict user preferences for unseen items

**Scalability**: Ensure the scalability and efficiency of the recommender system to handle large-scale datasets and serve real-time recommendations to users

**Evaluation**: Evaluate the performance of the recommender system using relevant metrics such as Hit Rate and ranking metrics like NDCG (Normalized Discounted Cumulative Gain), to assess the quality of recommendations.

**Data:**

Name: MovieLens dataset (contains users and movies with user ratings)
Samples: 100836
Number of Unique Users: 610
Number of Unique Movies: 9724
Number of Unique Genres: 951


## Training Setup:

- Install Dependencies mentioned in notebook
- run `training.ipynb` notebook on Jupyter or Visual Studio
- Set up CUDA for faster trianing, `Tesla 37C`(Single Machine) is used in our setup
- Trained model is saved on `model` folder with .pth extension

`training.ipynb` : Contains code to prepare data and train model
`EDA.ipynb` : Contains Exploratory data analysis on the entire data
`train.csv`, `evaluation.csv` : Contains 80:20 split of the entire dataset


Epoch: 10
Hidden Layers stack: [128,,64,32,16,8]
Total params: 12,441,185
batch_size = 32
Top k picks = 10

Our custom sequntial model with a stack of Linear layers and ReLU activation functions are trained for 10,12 epochs in different experimental setup. The best model parameters are given above.

Architecture:

![image](https://github.com/Venkata-Bhargavi/Recommender-System-Using-Neural-Networks/assets/114631063/2586e810-236c-4272-a56a-ce085aaef671)


## Results

We use the following metrics to evaluate the performance

NDCG :	Normalized discounted cumulative gain
HR :	Hit Rate

The following are the various experiemntal setup and their respective results

<img width="511" alt="image" src="https://github.com/Venkata-Bhargavi/Recommender-System-Using-Neural-Networks/assets/114631063/81a9009c-775f-44d8-a311-319c147c2c3e">


- Best performance has been recorded with the following setup
  
  <img width="637" alt="image" src="https://github.com/Venkata-Bhargavi/Recommender-System-Using-Neural-Networks/assets/114631063/f89328af-58e1-46f7-a03b-00388fd94f47">

**Re-Ranking:**

To further improve Hit Rate and NDCG scores, re-ranking techniques has been used to get best user specific recommendations in the top-k results. In this approach the recommended movies from the model are then reranked based on users interaction on the respective recommended image. This will highly help us in giving better recommendation in top-k results


Eg:  
Getting recommendations for userID : 453

Models HR and NDCG scores are

HR: 0.8
NDCG : 0.55

But, after re-ranking scores are 

HR : 1.0
NDCG: 1.0

<img width="615" alt="image" src="https://github.com/Venkata-Bhargavi/Recommender-System-Using-Neural-Networks/assets/114631063/871b4c68-68eb-47c8-a9db-67f7237283f1">







**GPU-Utilization:**

![image](https://github.com/Venkata-Bhargavi/Recommender-System-Using-Neural-Networks/assets/114631063/7f475b89-57b8-4a20-ab76-1bdd4f7e0e3f)

