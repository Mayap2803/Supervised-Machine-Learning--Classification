## Supervised-Machine-Learning-Classification

##### Libraries used: 
Sklearn, Matplotlib, Scipy, Numpy


### Project Aim: 

We want to train a range of supervised machine learning (ML) algorithms to classify particle events as signal and background events and determine the most suitable algorithm by evaluating their performances. 
Two datasets, Signal and Background, are provided, each containing 10,000 particle events, with each event corresponding to a correlated 3-dimensional feature vector ($\vec{x}$). 
The ML classification methods used include: [MLP](https://github.com/Mayap2803/Supervised-Machine-Learning--Classification/blob/main/MLP%20classifier.ipynb), [Linear Classifier](https://github.com/Mayap2803/Supervised-Machine-Learning--Classification/blob/main/Linear_classifier.ipynb), [K-Nearest Neighbours](https://github.com/Mayap2803/Supervised-Machine-Learning--Classification/blob/main/K_Nearest_Neighbour_Classifier.ipynb), [Boosted Decision Tree (Adaboost)](https://github.com/Mayap2803/Supervised-Machine-Learning--Classification/blob/main/Boosted_decision_tree_classifier.ipynb), and [Support Vector Machine (SVM)](https://github.com/Mayap2803/Supervised-Machine-Learning--Classification/blob/main/Support_vector_machine_classifier.ipynb).



### Method:

#### Manipulating the Datasets-
Two datasets are needed: one to train the ML algorithm and one to test the performance of the trained algorithm. 
To enable the algorithm to classify each particle event as either signal or background, target values of 1 and 0 were assigned, respectively, to each event through a separate array. 
The signal and background data were concatenated into a single array, and the same was done for the signal and background target values. 
Sklearn's 'train_test_split' function was used to randomly split the datasets into two equally sized training and test sets. 


#### Applying ML Algorithms-
The training dataset and its corresponding target values were used to train each algorithm using Sklearn's 'fit' function, followed by applying the 'predict' function on the test dataset to obtain a predicted target value array. 
The 'accuracy_score' function from the 'sklearn.metrics' library was then used to calculate the classificaton accuracy by comparing the predicted target values with the actual target values of the test dataset.


#### Visualising Each Algorithm's Performance: Scatter Plot and Histogram-
As the dataset contains a 3-dimensional feature vector, only the first two features were included in the code to display each algorithm's classification performance on a scatter plot and histogram. 
A scatter plot was used to display the background and signal events, shown in red and blue, respectively, with the optimal decision boundary, displayed as a black line, used by the trained algorithm to classify the events as either background or signal.
A histogram was used to illustrate the class separation, between background and signal events, predicted by the algorithm. The scatter plot and historgram for the MLP classifier are shown below.
<img src="https://github.com/user-attachments/assets/f532cdf2-ba35-42c5-9c49-9eb59266953a" alt="MLP scatterplot"> <img src="https://github.com/user-attachments/assets/8aeb7a40-b424-447c-98ed-2c73fecd5c29" alt="MLP decision function">




### Results:

The top three highest-performing algorithms were MLP with 3 hidden layers, each containing 7 nodes, SVM, and Boosted Decision Tree, with classification accuracies to $3.s.f$ of $0.915$, $0.891$, and $0.904$, respectively. 
