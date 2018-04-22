This repository is going to show how I have used a HIGHLY unbalanced dataset - the Credit Card Fraud Detection dataet - from Kaggle. This is the first time I am working on such a highly imbalanced dataset, and I am learning how to deal with such scenarios.
The dataset itself is huge, containing about 200k+ records. The target variables are 0 - for non fraudulent, and 1 - for fraudulent. The postive class 1 (fraudulent) accounts for only 0.17% of the whole datset.
How am I going to sample data for modelling when there is so much imbalance? The notebook shows what I have learnt and done to overcome the problem.

Things I've learnt today while working on this problem - 
1. If the event to be predicted belongs to a minority class and the event rate is less than 5%, it is referred to as a 'rare event', and this makes the data imbalanced.
2. Standard ML methods like Logistic Regression and Decision Trees do not work well with imbalanced data. They tend to predict the majority classes better, and treat the minority classes as NOISE. Hence, there is a HIGH probability of MISCLASSIFICATIO of the minority class as compared to the majority class.
3. Confusion matrix is not a viable method for checking the accuracy of a model for imbalanced datasets.
SAMPLING TECHNIQUES - This is used for imbalanced datasets. It reduces the instances of the MAJORITY class, or INCREASES the instances of the minority class.
Following are the sampling techniques that I have learnt - 
1. RANDOM UNDER-SAMPLING - Ramdomly REDUCES the instances of the MAJORITY class.
2. RANDOM OVER-SAMPLING - Ramdomly INCREASES the instances of the MINORITY class.
3. CLUSTER BASED OVER-SAMPLING - K-Means algorithm is applied independently to the minority and majority classes, and cluseters of each class is created. Each cluser is then over-sampled so that clusters of the same class have the  same number of instances and all classes have the same size.
4. Informed over-sampling - Syntethic Minority Over Sampling Technique (SMOTE) - This process creates synthetic samples of the minorty class, which are then added to the main dataset. This method prevents over-fitting caused by random sampling as we are using synthetic samples and not randomly replicating the minority classes instances. Also, no useful information is lost.
5. Modified Synthetic Minority Over Sampling Technique (MSMOTE)
