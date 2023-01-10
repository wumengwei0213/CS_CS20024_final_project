# CS_CS20024_final_project 

> 吳孟維 0816120

## Setup

Clone this repository

```clone
git clone https://github.com/wumengwei0213/CS_CS20024_final_project.git
```
## Requirements

To install requirements:

```setup
pip install -r requirements.txt
pip install jupyterlab
```

> In Windows 10 locally with Python 3.10

> Python 3.10.4 (tags/v3.10.4:9d38120, Mar 23 2022, 23:13:41) [MSC v.1929 64 bit (AMD64)]  
> Windows-10-10.0.19045-SP0  

## Training, Evaluation

To train and evaluate the model, run this command:

```train
cd CS_CS20024_final_project
jupyter-lab
```

> **Warning**
> If you just want to reproduce the prediction, it is no need to execute this file. It may fail.

> Execute [0816120_Final_train.ipynb](https://github.com/wumengwei0213/CS_CS20024_final_project/blob/34ee68394a940aeb41e535c5c7d6e301094cc7a9/0816120_Final_train.ipynb) You can see how it do training  

## Get the Prediction

> **Note**
> Please do it after installing the required module

> Execute [0816120_Final_inference.ipynb](https://github.com/wumengwei0213/CS_CS20024_final_project/blob/34ee68394a940aeb41e535c5c7d6e301094cc7a9/0816120_Final_inference.ipynb) You can see how it reproduce the prediction  

## Pre-trained Models

You can download pretrained models here:

- [CS_CS20024_final_project/goodmodel](https://github.com/wumengwei0213/CS_CS20024_final_project/tree/main/goodmodel)  

> Please put those models under the dir `/goodmodel`

## Results

My model achieves the following performance on :

### [Tabular Playground Series - Aug 2022](https://www.kaggle.com/competitions/tabular-playground-series-aug-2022/)

| Name         | Private Score | Public Score |
| ------------------ |---------------- | -------------- |
| inference.csv   |     0.59022         |      0.5803       |  

![](https://i.imgur.com/2GD780n.png)

## Brief Intro.  
>    After researching some discussion on the Kaggle, I have breif concept of this competition. I decide to design the NN model by myself in order to treat this project as a self-traing and strengthen my skill in machine learning region. With looking into the data, I found that feature "loading" has a great relationship with the goal. And the features that is categorical are not much assosiate with the goal, so I decided to drop these feature to focus on the numerial features. The crux that I can pass the baseline is adding "model assembling" at the end of training model. I chose models that got top-5 score in the Kaggle private leaderboard and re-made the prediction.
    
## Model Architecture  
![](https://i.imgur.com/DZCUs6I.png)  
### Hyperparameters  
> optimizer = Adam with learning_rate=0.001  
> loss = 'binary_crossentropy'  
> validation_split = 0.3  
> batch_size = 128  
> epochs = 10  
