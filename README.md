# Recommender-System-Using-Neural-Networks


## What is Recommender System, How is it achieved?
Recommender Systems are sophisticated algorithms designed to provide product-revelant-suggestions to users. These systems play a paramount role in enhancing user experience on various online platforms, including streaming services, e-commerce websites, socia media

They achieve this goal by analyzing past user interactions such as ratings, click, purchases. These algorithms can be collaborative (based on user interaction) or content-based (item features). 

**Objective:**


**Data:**



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

To further improve Hit Rate and NDCG scores, re-ranking techniques has been used to get best user specific recommendations in the top-k results.

