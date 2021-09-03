# CBM-Particle-Identification
### About
The model predicts the Signal (Muons) from the background noise of the output of CBM(Compressed Baryonic Matter) detector
### Dataset
The dataset has been directly obtained from CERN for practice purpose.The dataset conatins 16 columns and 215343 rows.All the columns present are numerical 
### Data Preprocessing
There were some outliers present in the data which were removed by using IQR and Boxplot.Various visualizations were made to understand the signal to background ratio for each column.The distribution for the various columns were explored and I featured engineered a column "mass" by combining other four columns,the correlation of this new custom generated column was found to be greater than the correalation of any of the four columns that we considered.I was able to construct a new feature "Mass" because I had domain knowledge about it.
<br>
<img src="https://github.com/nilay121/Particle-Identification/blob/main/kde plot.png">
### Model Creation
I wrote a Custom SVM Class to test how it performs with the SVM of Scikit Learn and other ML models.I considered three models for this task Custom SVM, SVM Sklearn and Random Forest Classifier.I trained all the three models with default parameters and tested it on the validation set.SVM of Sklearn and Random forest performed nearly the same but the
custom SVM had accuracy little lesser than the other two models.

### Performance Metric
I used F1 score as the performance metric,because I wanted to consider the imporatnce of both precision and recall.SVM and Random Forest had same F1 score of 0.97 but Custom
SVM class had F1 score of 0.92. I also plotted the ROC-AUC curve to get a more visual feeling of the results obtained.
<br>
<img src="https://github.com/nilay121/Particle-Identification/blob/main/git.png">
ROC-AUC

