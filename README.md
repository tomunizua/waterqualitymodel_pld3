<h1>WATER QUALITY MODEL</h1><br>
<h2>Introduction</h2><br>

This repository contains a machine learning model designed to predict the potability of water based on various quality parameters. The model utilizes a combination of data preprocessing techniques, neural network architecture, and performance evaluation metrics to ensure accurate and reliable predictions. Three(3) different optimizers were used in buildiing 3 different models to analyze the accuracy that will be gotten from each model.

<h3>DATASET</h3>
This dataset contains water quality measurements and assessments related to potability, which is the suitability of water for human consumption. The dataset's primary objective is to provide insights into water quality parameters and assist in determining whether the water is potable or not. Each row in the dataset represents a water sample with specific attributes, and the "Potability" column indicates whether the water is suitable for consumption.

https://www.kaggle.com/datasets/uom190346a/water-quality-and-potability?select=water_potability.csv

<h3>MODEL ARCHITECTURE DESCRIPTION AND EXPLANATION OF OUTPUTS - BERNICE AWINPANG AKUDBILLA</h3><br>
    
This model consists of four hidden layers with 64, 32, 16, and 8 neurons, all using ReLU activation and L2 regularization (l2(0.0001)) to prevent overfitting by discouraging large weights. A dropout rate of 30% is applied after the first two hidden layers to reduce overfitting by randomly deactivating neurons during training, ensuring better generalization. The optimizer chosen is Stochastic Gradient Descent (SGD) with gradient clipping (clipnorm=1.0), which helps stabilize training and prevent exploding gradients, while early stopping monitors validation loss and halts training if it stops improving for 10 consecutive epochs

<h4>Bernice's Summary table</h4><br>

| Train Instance | Engineer Name     | Regularizer | Optimizer | Early Stopping | Dropout Rate | Accuracy | F1 Score        | Recall         | Precision      |
|----------------|-------------------|-------------|-----------|----------------|--------------|----------|-----------------|----------------|----------------|
| Model 1        | Bernice  Akudbilla | L2          | SGD      | Yes            | 0.3          | 0.628    | 0- 0.76, 1- 0.22| 0- 0.92, 1-0.14| 0- 0.64, 1-0.54|
    
<br>

<h4>RESULTS AND ANALYSIS</h4><br>
my model is the best as compared to the other models with an accuracy of 0.628 because of the use of SGD with gradient clipping( clipnorm=1.0) which helped stabilizing the training and prevented drastic weight updates, allowing for better generalization compared to RMSprop and Adam, which probably have over-learned the training data. Additionally, my model effectively captured patterns in both classes, as seen in its recall and precision scores(0.92,0.14),(0.64,0.54) respectively. Although my model performed porely in predicting class 1,it did relatively better as compared to the other models which failed to learn meaningful representations, it is most likely due to ineffective weight updates or poor adaptation to class imbalances.
<br>

<h3>MODEL ARCHITECTURE DESCRIPTION AND EXPLANATION OF OUTPUTS - Theodora Omunizua<h3><br>
    
Insights from Experiments/Challenges: I ended up with zero values for F1 score, precision and recall so I tried fixing this by changing the neural network structure, increasing+reducing the learning and dropout rates, but then realized the problem was class imbalance, my model was not predicting any positives.
Parameter Choices: Learning rate of 0.001 to avoid overshooting, Dropout rate of 0.3 to prevent overfitting, and Early Stopping patience of 10 epochs to monitor validation loss and to stop training when the line flattens
<h4>THEODORA's Summary table</h4><br>
    
| Train Instance | Engineer Name     | Regularizer | Optimizer | Early Stopping | Dropout Rate | Accuracy   | F1 Score | Recall | Precision |
|----------------|-------------------|-------------|-----------|----------------|--------------|------------|----------|--------|-----------|
| Model 2        | Theodora Omunizua | L2          | Adam      | Yes            | 0.3          | 0.624      | 0.0      | 0.0    | 0.0       |

<br>
<h4>RESULTS AND ANALYSIS</h4>
While the accuracy scores of all three models are similar, Bernice's model shows better performance through its non-zero values for F1 scores, recall and precision as compared to the other two models. Ruth and I's models have an F1 score, recall, and precision of 0.0, indicating no positive predictions were made. This shows that the models struggled with class imbalance, resulting in poor predictions (zero values) for the minority class. Adjusting class weights and exploring different regularization techniques could improve performance.
Also, Bernice's model uses SGD for optimization, which might have provided better generalization on the dataset compared to the Adam optimizer I used, and RMSprop optimizers Ruth used. SGD can sometimes offer advantages in sparse or noisy data settings.
<br>
  
<h3>MODEL ARCHITECTURE DESCRIPTION AND EXPLANATION OF OUTPUTS - Iradukunda Ruth <h3><br>
    
<h4>RUTH's Summary TABLE</h4><br>

| Train Instance | Engineer Name   | Regulariez | Optimizer | Early stopping | Dropout Rate | Accuracy | F1 Score | Recall | Precision |
|----------------|-----------------|------------|-----------|----------------|--------------|----------|----------|--------|-----------|
| Model 3        | Iradukunda Ruth | L2         | RMSprop   | Yes            | 0.3          | 0.6      | 0.0      | 0.0    | 0.0       |

<h4>RESULTS AND ANALYSIS</h4>

