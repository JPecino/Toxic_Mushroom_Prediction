# Mushrooms! Edible or Poisonous

 ## Team Members
 - [Emily Boulware](https://github.com/emilymees)
 - [Shelby Reyes-Widrick](https://github.com/slreyesw)
 - [Jackeline Larios](https://github.com/jl211412)
 - [Julian Pecino](https://github.com/JPecino)

## Project Overview
Wild mushroom identification plays a critical role for anyone foraging the wilderness for their food, and while there are many species of mushrooms that are safe for human consumption, there are also those that can cause adverse, possibly severe, effects if ingested. The objective of this machine learning project is to develop a model that can accurately classify mushrooms as either edible or poisonous based on their physical characteristics. 

## Data
The dataset used to train our machine learning model is from UC Irvine and contained 8,124 rows of data. This included many different features of mushrooms, including cap shape, cap surface, cap color, bruises, odor, gill-attachment, gill spacing, gill size, gill color, stalk shape, stalk root, stalk surfaces above and below ring, veil types, veil colors, ring numbers, ring types, spore print colors, population, and habitat. 

## Steps  
The dataset initially contained abbreviated values for each mushroom feature column so we determined expanding these fields to the full value name would help everyone read the data without a key legend. 
We then determined we would be able to remove the "veil-type" column from the data set since every mushroom tested in the dataset had a partial veil feature. 

Since "poisonous" and "edible" were provided as "class" values in the dataset we concluded this column would be our target vector and the remaining columns would be our features. 

![Alt text](https://github.com/JPecino/Toxic_Mushroom_Prediction/blob/main/Resources/Images/vector_features.png)

After encoding and then scaling the features, our machine learning model was first trained with the K-Nearest Neighbor algorithm. We decided to start with this algorithm since it can be an ideal option for non-linear data and no assumptions would be made regarding underlying data. As shown, this model performed exceptionally well! 

![Alt text](https://github.com/JPecino/Toxic_Mushroom_Prediction/blob/main/Resources/Images/knn_report.png)

Given that our first model performance significantly exceeded our expectations, we decided to train our machine learning model with a few different algorithms to possibly help reduce overfitting and confirm accuracy. 
We were pleasantly surprised to see that the results using Decision Tree and Random Forest algorithms also showed excellent accuracy scores over 99%.

![Alt text](https://github.com/JPecino/Toxic_Mushroom_Prediction/blob/main/Resources/Images/decisiontree_report.png)

![Alt text](https://github.com/JPecino/Toxic_Mushroom_Prediction/blob/main/Resources/Images/randomforest_report.png)

Since our dataset was so balanced and the machine learning models' performance exceeded our expectations we then narrowed down the top siginificant features in the dataset and based our last model training on this smaller subset. We saw no decrease in performance and determined our model would continue to consistently deliver dependable results.

![Alt text](https://github.com/JPecino/Toxic_Mushroom_Prediction/blob/main/Resources/Images/imp_features.png)

![Alt text](https://github.com/JPecino/Toxic_Mushroom_Prediction/blob/main/Resources/Images/decisiontree_imp_report.png)


## Conclusion
We tested three models including Kneighbors, Random Forest, and Decision Tree. All three models were able to predict which mushrooms were edible or posionous, based on the various features listed above, at 99% to 100% accuracy. The most important features overall in determining if a mushroom was edible or poisonous were odor, gill size, bruises, texture of stalk surface, and spore color.

## References
UCI Machine Learning. April 1987. Mushroom Classification, 2016. Retrieved October 5, 2023 from https://www.kaggle.com/datasets/uciml/mushroom-classification
