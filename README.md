# ML_Project_Classification_Breast-Cancer
In this problem, I work with the Breast Cancer Wisconsin (Diagnostic) dataset. The dataset contains thirty features, and they are obtained from a digitized image of a fine needle aspirate (FNA) of a breast mass. The rows are labeled as M and B, where M stands for Malignant and B for Benign. The purpose of this project is the prediction of the type of the cancer (M and B) using three classification models: Logistic Regression (LR), Support Vector Machine (SVM), and XGBOOST. Here is the link to the dataset: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

# Data Cleaning
The dataset contains a column (Unnamed) with NaN values which needs to be removed. We checked the outliers and removed the rows below 10% quantile and above 90% quantile. 
Using feature selection method and checking the cross-correlations between the features, we selected eight features in our models. 

# Models:
Three models have been tested to identify the type of breast cancer: **LR**, **SVM**, and **XGBOOST**.
In these models, grid-search was used to find the optimal values for the parameters in building the models. "f1-score" and "recall" were chosen as the scoring parameters in the grid-search.

# Results:
Three models perform quite well with similar accuracies (0.94-0.96). In this problem, it is important that the model results in a low misclassification for Malignant type since the life of the person is at stake. This can be checked by looking at the confusion matrix and calculating the "recall" score.
We can see that SVM model outperforms LR and XGBOOST models by 2% in "recall". SVM misclassifies two malignant cases as benign and XGBOOST and LR both misclassify three Malignant cases as benign tumor cell type.
The number of misclassified cases for benign resulting from SVM, XGBOOST and LR models are eight, five, and one, respectively.
