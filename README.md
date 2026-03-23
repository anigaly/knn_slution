k-Nearest Neighbours (kNN)
Classification Project


1. Dataset Selection
For this project, I selected the Iris dataset from sklearn.datasets. The dataset contains
150 samples with 4 numerical features (sepal length, sepal width, petal length, petal width)
and 3 balanced classes representing different iris species.
I chose this dataset because:


● It is clean and requires minimal preprocessing.
● It contains meaningful numerical features.
● It is suitable for demonstrating how kNN behaves under different values of k.
● It allows clear visualisation and interpretation of results.


2. Problem Type
This project focuses on a multi-class classification problem.
The objective is to correctly classify iris flowers into one of three species using the k-Nearest
Neighbours algorithm.


3. Data Preprocessing
The following preprocessing steps were applied:
● Train/Test split (80% training, 20% testing).
● Feature scaling using StandardScaler.
Feature scaling is essential for kNN because the algorithm is distance-based. Without
scaling, features with larger numeric ranges would dominate the distance calculations and
negatively affect model performance.


4. Hyperparameter Selection
To determine the optimal model configuration, I performed cross-validation using
GridSearchCV.
The following hyperparameters were tested:
● k values from 1 to 30
● Distance metrics: Euclidean and Manhattan
Cross-validation (5-fold) was used to ensure that the model generalises well and does not
overfit to a specific training subset.
The best model was selected based on the highest cross-validation accuracy.


5. Best Model Configuration
● Best k: (insert your value here)
● Best distance metric: (insert your metric here)
● Best cross-validation accuracy: (insert value)
● Test accuracy: (insert value)
The results show that moderate values of k provide the best generalisation performance.
Small k values tend to overfit (high variance), while very large k values may underfit (high
bias). This behaviour illustrates the bias–variance tradeoff.


6. Model Evaluation
The final model was evaluated using:
● Accuracy
● Confusion Matrix
The confusion matrix shows that most misclassifications occur between similar species,
which indicates that the model struggles slightly when class boundaries overlap.


7. What I Learned
Through this project, I learned:
● The importance of feature scaling in distance-based algorithms.
● How cross-validation improves model selection.
● How the choice of k affects bias and variance.
● The impact of different distance metrics on classification performance.
This project strengthened my understanding of how kNN works in practice and how model
performance depends on hyperparameter tuning.



8. Limitations
Despite good performance, kNN has several limitations:
● It is computationally expensive for large datasets.
● It requires storing the entire training dataset (memory-based).
● It is sensitive to irrelevant or noisy features.
● Performance may degrade in high-dimensional spaces (curse of dimensionality).
