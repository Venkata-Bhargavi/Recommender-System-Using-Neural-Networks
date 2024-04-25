# Recommender-System-Using-Neural-Networks


## What is Recommender System, How is it achieved?
Recommender Systems are sophisticated algorithms designed to provide product-revelant-suggestions to users. These systems play a paramount role in enhancing user experience on various online platforms, including streaming services, e-commerce websites, socia media

They achieve this goal by analyzing past user interactions such as ratings, click, purchases. These algorithms can be collaborative (based on user interaction) or content-based (item features). 



## Training Setup:

- Install Dependencies mentioned in notebook
- run `training.ipynb` notebook on Jupyter or Visual Studio
- Set up CUDA for faster trianing, `Tesla 37C`(Single Machine) is used in our setup
- Trained model is saved on `model` folder with .pth extension

`training.ipynb` : Contains code to prepare data and train model
`EDA.ipynb` : Contains Exploratory data analysis on the entire data
`train.csv`, `evaluation.csv` : Contains 80:20 split of the entire dataset



