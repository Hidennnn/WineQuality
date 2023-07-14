# WineQuality

## Technology
|    **Name**    | **Version** |
|:--------------:|:-----------:|
|    `Python`    |   3.10.0    |
| `scikit-learn` |    1.2.2    |
|    `pandas`    |    1.5.3    |
|    `numpy`     |   1.25.0    |
|  `matplotlib`  |    3.7.1    |
|   `seaborn`    |   0.12.2    |

## Description
Thanks the project I learnt about EDA and build models in 
sklearn for category prediction. 

## Database
In the project I worked with the Wine Quality database. 
Project's goal was prediction of quality of wine. I split
the project on 2 parts.

1. Predict if a wine is good or bad.
2. Predict detailed wine's quality.

**Link to database:**
https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009

## Results

### *1st part*
In 1st part RandomForestClassifier achieved the best results.

**Params**:

|      **Name**       | **Value** |
|:-------------------:|:---------:|
|    `n_estimator`    |    442    |
|     `criterion`     | log_loss  |
|     `max_depth`     |   None    |
| `min_samples_leaf`  |     2     |
| `min_samples_split` |     4     |

**Accuracy**: 85%

**Precision**:
- *good*: &nbsp;85%
- *bad*: &nbsp;&nbsp;&nbsp;85%

**Recall**:
- *good*: &nbsp;80%
- *bad*: &nbsp;&nbsp;&nbsp;87%

### *2nd part*
In the 2nd part I used the same model and the same params
which was the best in 1st part.

**Accuracy**: 70%

**Precision**:
- *0*: &nbsp;&nbsp;&nbsp;0%
- *1*: &nbsp;&nbsp;&nbsp;0%
- *2*: &nbsp;73%
- *3*: &nbsp;68%
- *4*: &nbsp;64%
- *5*: &nbsp;&nbsp;&nbsp;0%

**Recall**:
- *0*: &nbsp;&nbsp;&nbsp;0%
- *1*: &nbsp;&nbsp;&nbsp;0%
- *2*: &nbsp;81%
- *3*: &nbsp;77%
- *4*: &nbsp;50%
- *5*: &nbsp;&nbsp;&nbsp;0%

## Summary

The model works quite good for grouped cases,
but not for detailed groups. Even if accuracy
is about 70%, the model has problems with 
other quality than 2 and 3. 