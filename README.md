# Credit Risk Analysis  
## Overview  
The purpose of this analysis is to apply machine learning to evaluate a credit card credit dataset from LendingClub to predict credit risk.  Six models were used:  

* RandomOverSampler
* SMOTE
* Cluster Centroids
* SMOTEENN
* Balanced Random Forest Classifier
* Easy Ensemble Classifer

## Results  
### Random Over Sampler  
![randomoversample-conf](https://user-images.githubusercontent.com/88070999/145698872-a3fba8cc-e3fa-427f-b7d9-be5df89c538f.png)

![randomoversample-BA](https://user-images.githubusercontent.com/88070999/145698875-6503d40c-7a6d-4b1a-94d8-8cd107c2d509.png)

For the RandomOverSampler model:
* Overall precision is high for low risk (1.00) but low for high risk (.01).
* F1 Score is .75 overall, but .02 for high risk.
* Recall average is .6

### SMOTE  
![smot-conf](https://user-images.githubusercontent.com/88070999/145698876-8141ee18-c96f-4234-8e78-69d8970e24d9.png)

![smot-BA](https://user-images.githubusercontent.com/88070999/145698878-7fda69cf-2d3b-4da0-8277-508c198ce0e9.png)

For the SMOTE model:
* Overall precision is .99
* F1 Score is .81 overall
* Recall average is .69

### Cluster Centroids  
![centroids-conf](https://user-images.githubusercontent.com/88070999/145698880-efd48f0e-243f-4479-b660-0f6550fc6311.png)

![centroids-ba](https://user-images.githubusercontent.com/88070999/145698882-ecbc4c5e-da2f-4de2-a3e9-8924c053dafe.png)
For the Cluster Centroids model:
* Overall precision is .99
* F1 Score is .56 overall
* Recall average is .40

### SMOTEENN  
![smoteenn-conf](https://user-images.githubusercontent.com/88070999/145698890-2c6e9893-f541-40e0-a1c0-fd3d06bec029.png)

![smoteenn-BA](https://user-images.githubusercontent.com/88070999/145698892-9799a313-c7d7-4fad-8628-1775552c84f9.png)
For the SMOTEENN model:
* Overall precision is .99
* F1 Score is .73 overall
* Recall average is .58

### Balanced Random Forest Classifier  
![balanced-conf](https://user-images.githubusercontent.com/88070999/145698894-51aa9c18-014a-4fe9-b4bc-fd036c2c1bb1.png)

![balanced-BA](https://user-images.githubusercontent.com/88070999/145698898-74b8bed1-c549-4b67-9502-97c9ad7c6030.png)
For the Balanced Random Forest model:
* Overall precision is .99
* F1 Score is .94 overall
* Recall average is .89

### Easy Ensemble Classifer  
![easyens-conf](https://user-images.githubusercontent.com/88070999/145698900-9160020d-1099-4ddf-ab37-7b7f634c9417.png)

![easyens-BA](https://user-images.githubusercontent.com/88070999/145698901-c06ba0db-8baa-45ba-bbb6-05a210caf8b6.png)

For the Easy Ensemble Classifier model:
* Overall precision is .99
* F1 Score is .97 overall
* Recall average is .94


## Summary  
In summary, all of the models showed an overall precision score of .99.  This calculation is the true positives divided by all positives.  In other words, the models were all precise in terms of minimizing the number of false positives.  

Regarding recall, this calculation is a ratio of the true positives divided by (true positives + false negatives).  This might be better understood as "I know there is high credit risk, so what is the likelihood that the model will find it?  The lowest performing model was cluster centroids, whereas the highest was easy ensemble classifier.  

The F1 score is a way to combine the two scores for a model.  A low score indicates an imbalance between the two.  In this case, the lowest performing model was the cluster centroids at .56, and the highest was the easy ensemble classifier at .97.


### Recommendation  
Overall, the model with the best results was the Easy Ensemble Classifier model.  This model had an overall precision of 0.99, like the other models.  However, the recall average of .94, combined with the F1 score of .97, makes this the most effective model to use for this purpose.
