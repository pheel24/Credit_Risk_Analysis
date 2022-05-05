# Credit_Risk_Analysis

## Overview
In this project, we assesed the utility of a few supervised machine learning models with respect to credit risk. We started with oversampling and undersampling models, then we combined these two approaches, and finally we used bias-reducing models. The goal was to compare these models and see which ones worked the best with such a feature-heavy dataset.

## Results

### RandomOverSampler model

![model1_accuracy](https://user-images.githubusercontent.com/95315957/165871789-d9091a85-dd84-4ee6-9b1e-f2975902edbe.PNG)

![model1_cm](https://user-images.githubusercontent.com/95315957/165871798-0970f9f6-7751-4059-bad5-e8e63b41707a.PNG)

![model1_icr](https://user-images.githubusercontent.com/95315957/165871815-8d7de1d9-69ad-4eb8-924f-dbb387ad63a2.PNG)

For the first model, the accuracy score was 62%, with a high_risk precision score of 1% and a sensitivity score of 60%. This yielded an f1 score of 2%. With the higher number of low_risk entries, the precision approached 100% with a sensitivity of 65%.

### SMOTE model

![model2_accuracy](https://user-images.githubusercontent.com/95315957/166972661-c346aca0-a69e-4d1c-9e7c-d95c09a8f6a9.PNG)

![model2_cm](https://user-images.githubusercontent.com/95315957/166972690-ac024d83-898d-460a-ba92-9dbfa09f961d.PNG)

![model2_icr](https://user-images.githubusercontent.com/95315957/166972716-06835f91-7ae0-41eb-9253-3e5c8dad3658.PNG)

For the second model utilizing a SMOTE algorithim, the accuracy was 65%, with scores of 1%  and 64% for precision and sensitivity respectively. This yielded an f1 score of 2% for the high_risk catagory. For the low_risk catagory, the precision approached 100% with sensitivity at 66%. Overall, this model was quite similar to the first.

### ClusterCentroid Model

![model3_accuracy](https://user-images.githubusercontent.com/95315957/166973680-896d5e56-2133-4182-99f6-d0c5af6afcf6.PNG)

![model3_cm](https://user-images.githubusercontent.com/95315957/166973710-b292226c-d14a-473c-be60-06d4980175d5.PNG)

![model3_icr](https://user-images.githubusercontent.com/95315957/166973725-4dd2aa0d-7348-44b1-9c60-2fb14069bc51.PNG)

For our third model, the balanced accuracy score was 51%. For the high_risk catagory, the precision and sensitivity scores were 1% and 60% respectively, yielding an f1 score of 1%. 
For the low_risk catagory, the precision and sensitivity scores were ~1 and 43% respectively, seemingly due to the high rate of false positives within this model. 

### SMOTEENN Model

![model4_accuracy](https://user-images.githubusercontent.com/95315957/166974966-3f005524-963b-45c2-b11e-7803c6a49cbe.PNG)

![model4_cm](https://user-images.githubusercontent.com/95315957/166974991-33ce677a-32eb-4654-98c3-e30f4fef1e28.PNG)

![model4_icr](https://user-images.githubusercontent.com/95315957/166975011-eabf18f7-6660-4d61-9a3a-222c5a5f004a.PNG)

For our fourth model, the balanced accuracy score was 61%. For the high_risk catagory, the precision and sensitivity scores were 1% and 69% respectively, yielding an f1 score of 2%. 
For the low_risk catagory, the precision and sensitivity scores were ~1 and 54% respectively.

### BalancedRandomForestClassifier Model

![model5_accuracy](https://user-images.githubusercontent.com/95315957/166975650-8f95c5c2-efbd-4f80-a7c4-b3481c6f8f60.PNG)

![model5_cm](https://user-images.githubusercontent.com/95315957/166975669-2cd2c3c8-5930-4c1f-9177-7563c04f0e3b.PNG)

![model5_icr](https://user-images.githubusercontent.com/95315957/166975673-6d7f98c3-0bc0-44de-b775-b2def5a41fbc.PNG)

For our fifth model, the balanced accuracy score was 78%. For the high_risk catagory, the precision and sensitivity scores were 4% and 67% respectively, yielding an f1 score of 7%.
For the low_risk catagory, the precision and sensitivity scores were ~1 and 91% respectively.

### EasyEnsembleClassifier Model

![model6_accuracy](https://user-images.githubusercontent.com/95315957/166976231-81e95949-d358-451f-83bc-43fa8e6ff608.PNG)

![model6_cm](https://user-images.githubusercontent.com/95315957/166976241-89715e82-15e8-499a-8a6e-d6423aa9ec4c.PNG)

![model6_icr](https://user-images.githubusercontent.com/95315957/166976260-c0ace1ba-dcb0-48a7-a71a-98b98e4df899.PNG)

For our sixth model, the balanced accuracy score was 92%. For the high_risk catagory, the precision and sensitivity scores were 7% and 91% respectively, yielding an f1 score of 7%.
For the low_risk catagory, the precision and sensitivity scores were ~1 and 94% respectively.

## Summary
A trend running through all the models is low-precision in the high_risk catagory, while this is improved by the ensemble models, the precision still remains low. This means that while the later models can classify high_risk entries fairly well, there will be many wrongly classified low_risk entries. For this reason, these models would be sub-optimal as the basis for a lending stratedgy, as many profitable customers would potentially turned away. 
