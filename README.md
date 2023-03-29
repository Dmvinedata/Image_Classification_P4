# Image_Classification_p4
Phase 4 Project 4 Image Classification
[Presentation Link](https://github.com/Dmvinedata/Image_Classification_P4/blob/main/P4_Presentation.pdf) <br>

[Jupyter Notebook Link](https://github.com/Dmvinedata/Image_Classification_P4/blob/main/notebook.pdf)  <br>

## Author: Deztany Jackson


# Overview


***
![Pneumonia](https://github.com/Dmvinedata/Image_Classification_P4/blob/main/images/Pneumonia.jpeg)
***

# Business Understanding
A local hospital wants to explore their image recognition options for pneumonia cases. They want eventually replace a few doctors due to staffing issues. They want to test it out for a trial version.


# Data Understanding
The dataset is from Chest X-Ray of "Normal" and "Pneumonia" images from [Kaggle](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) with a total of 5856 .jpeg files. This data set is already broken up into three folders (train, validation and test) and a folder for each category ("NORMAL" or "PNEUMONIA").

Based on the business goal and data, the main metrics will be Recall, F1-Score, and Loss, Accuracy will be secondary.

# Modeling
Iteratively produce models. As new information was learned new models, parameters and transformation techniques were applied.

- Model 1 Baseline
- Model 2-3 Baseline Modification 
- Model 4-7 Hyperparameter optimization 
- Model 8-10 Transfer Learning
- Final Model (Model 5)                                     
## Results
From the 624 Data pieces:<br>
    - .59% True Positive (366)<br>
    - .014% True Negative (9)<br>
    - .04% False Negative (24)<br>
    - .36% False Positive (225)<br>
    
Normal:<br>
    - Recall:.04 <br>
    - F1-Score:.07 <br>

Pneumonia:<br>
    - Recall:.94 <br>
    - F1-Score:.75 <br>
- Loss:.68
- Accuracy:.6

### Test Prediction Confusion Matrix

***
![Confusion Matrix](https://github.com/Dmvinedata/Image_Classification_P4/blob/main/images/Test_PRed.png)
***

### True Positive Evaluation
***
![True Positive Eval](https://github.com/Dmvinedata/Image_Classification_P4/blob/main/images/TP_Lime.jpg)
***

# Conclusion

## Limitation
Hospital:
- Important image areas
- Radiologist SME knowledge

Technical:

- Hardware and Software Compatibility (Modeling on M2 GPU Laptop)
- Hyperparameter optimization limits
- Blackbox of Hidden Layers


## Reccomendation

Hospital:

- Usage: The model is best as a learning tool and not an official diagnosis.
- Strategy: Use the model as an initial reviewer of the images.
- Staffing: The model is best used with a doctor, not standalone.

Technical:

- Scope, review and process images more beforehand
- Visualize the activation functions to see better what areas the model layers are diagnosing
- Iterate model improvement with with augmented data
- Visually inspect the images that were FN and FP.

   

