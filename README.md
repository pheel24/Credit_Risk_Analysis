# Credit_Risk_Analysis

## Overview
In this project, we assesed the utility of a few supervised machine learning models with respect to credit risk. We started with oversampling and undersampling models, then we combined these two approaches, and finally we used bias-reducing models. The goal was to compare these models and see which ones worked the best with such a feature-heavy dataset.

## Results

#RandomOverSampler model

![model1_accuracy](https://user-images.githubusercontent.com/95315957/165871789-d9091a85-dd84-4ee6-9b1e-f2975902edbe.PNG)

![model1_cm](https://user-images.githubusercontent.com/95315957/165871798-0970f9f6-7751-4059-bad5-e8e63b41707a.PNG)

![model1_icr](https://user-images.githubusercontent.com/95315957/165871815-8d7de1d9-69ad-4eb8-924f-dbb387ad63a2.PNG)

For the first model, the accuracy score was 62%, with a high_risk precision score of 1% and a sensitivity score of 60%. This yielded an f1 score of 2%. With the higher number of low_risk entries, the precision approached 100% with a sensitivity of 65%.

#SMOTE model

![model2_accuracy](https://user-images.githubusercontent.com/95315957/166972661-c346aca0-a69e-4d1c-9e7c-d95c09a8f6a9.PNG)

![model2_cm](https://user-images.githubusercontent.com/95315957/166972690-ac024d83-898d-460a-ba92-9dbfa09f961d.PNG)

![model2_icr](https://user-images.githubusercontent.com/95315957/166972716-06835f91-7ae0-41eb-9253-3e5c8dad3658.PNG)

For the second model utilizing a SMOTE algorithim, the accuracy was 65%, with scores of 1%  and 64% for precision and sensitivity respectively. This yielded an f1 score of 2% for the high_risk catagory. For the low_risk catagory, the precision approached 100% with sensitivity at 66%. Overall, this model was quite similar to the first.

#ClusterCentroid Model

![model3_accuracy](https://user-images.githubusercontent.com/95315957/166973680-896d5e56-2133-4182-99f6-d0c5af6afcf6.PNG)

![model3_cm](https://user-images.githubusercontent.com/95315957/166973710-b292226c-d14a-473c-be60-06d4980175d5.PNG)

![model3_icr](https://user-images.githubusercontent.com/95315957/166973725-4dd2aa0d-7348-44b1-9c60-2fb14069bc51.PNG)

