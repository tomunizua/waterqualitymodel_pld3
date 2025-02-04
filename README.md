<h1>WATER QUALITY MODEL</h1><br>
<h2>Introduction</h2><br>

This repository contains a machine learning model designed to predict the potability of water based on various quality parameters. The model utilizes a combination of data preprocessing techniques, neural network architecture, and performance evaluation metrics to ensure accurate and reliable predictions.

<h3>MODEL ARCHITECTURE DESCRIPTION AND EXPLANATION OF OUTPUTS</h3><br>
    
This model consists of four hidden layers with 64, 32, 16, and 8 neurons, all using ReLU activation and L2 regularization (l2(0.0001)) to prevent overfitting by discouraging large weights. A dropout rate of 30% is applied after the first two hidden layers to reduce overfitting by randomly deactivating neurons during training, ensuring better generalization. The optimizer chosen is Stochastic Gradient Descent (SGD) with gradient clipping (clipnorm=1.0), which helps stabilize training and prevent exploding gradients, while early stopping monitors validation loss and halts training if it stops improving for 10 consecutive epochs

<h4>Bernice's Summary table</h4><br>

| Train Instance | Engineer Name     | Regularizer | Optimizer | Early Stopping | Dropout Rate | Accuracy | F1 Score        | Recall         | Precision      |
|----------------|-------------------|-------------|-----------|----------------|--------------|----------|-----------------|----------------|----------------|
| Model 1        | Bernice  Akudbilla | L2          | SGD      | Yes            | 0.3          | 0.628    | 0- 0.76, 1- 0.22| 0- 0.92, 1-0.14| 0- 0.64, 1-0.54|
    
<br>

<h4>RESULTS AND ANALYSIS</h4><br>
my model performed better because the use of SGD with gradient clipping( clipnorm=1.0) which helped stabilizing the training and prevented drastic weight updates, allowing for better generalization compared to RMSprop and Adam, which probably have over-learned the training data. Additionally, my model effectively captured patterns in both classes, as seen in its recall and precision scores(0.92,0.14),(0.64,0.54) respectively. Although my model performed porely in predicting class 1,it did relatively better as compared to the other models which failed to learn meaningful representations, it is most likely due to ineffective weight updates or poor adaptation to class imbalances.

<h3>MODEL ARCHITECTURE DESCRIPTION AND EXPLANATION OF OUTPUTS<h3><br>

  
<h4>THEODORA's Summary table</h4><br>
    
| Train Instance | Engineer Name     | Regularizer | Optimizer | Early Stopping | Dropout Rate | Accuracy | F1 Score | Recall | Precision |
|----------------|-------------------|-------------|-----------|----------------|--------------|----------|----------|--------|-----------|
| Model 2        | Theodora Omunizua | L2          | Adam      | Yes            | 0.3          | 0.6      | 0.0      | 0.0    | 0.0       |

<br>

<h4>RESULTS AND ANALYSIS</h4>

  
<h3>MODEL ARCHITECTURE DESCRIPTION AND EXPLANATION OF OUTPUTS<h3>


  
<h4>RUTH's Summary TABLE</h4><br>

| Train Instance | Engineer Name   | Regulariez | Optimizer | Early stopping | Dropout Rate | Accuracy | F1 Score | Recall | Precision |
|----------------|-----------------|------------|-----------|----------------|--------------|----------|----------|--------|-----------|
| Model 3        | Iradukunda Ruth | L2         | RMSprop   | Yes            | 0.3          | 0.6      | 0.0      | 0.0    | 0.0       |

<h4>RESULTS AND ANALYSIS</h4>

