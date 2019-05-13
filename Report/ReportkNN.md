kNN Machine Learning Error Analysis Report
===========

##### Authors: Emilie Dubé and Aidan Zentner
##### Professors Sameer Bhatnager and Jean-François Brière

##### Intro to Computer Programming in Engineering and Science

##### 360-420-DW Section 02

##### May 14 2019

Distributions of Model Accuracy: Confidence in Model
-------------------
*Why do we get a different accuracy each time we run the classification model?*

In DataSet.java, lines 148 to 150 explain why the accuracy each time the classification model is run is different. 
In java, the class method '.shuffle' from the 'Collections' class accesses different elements randomly from a given String.
Thus, each time we cut the data set, we work with a different section of data. This affects the accuracy of the overall results.

*How much does performance vary on unseen data?*

Performance varies slightly every time the classification model is run. The standard deviation is particularly low.

Mean: 0.9695620437956158

STD: 1.7353615003463184 x 10^-4

*What is a sensible baseline against which we should compare our model's performance?*

A sensible baseline to use to compare our model's performance is that of random identification. If the majority of data shows positive,
then it is safe to run the classification as though all of the data is positive. This way, we will get a maximum accuracy equal to the actual number
of positive data. This is an obvious and simple baseline.

Line 200 in DataSet.java details a method that prints a label indicating the frequency of a given label. So, if we identify the frequency of a certain label to be,
say, 70%, then we can safely say that, by running as though all data is that certain label, we will have 70% accuracy.

Analysis of Different Error Types
-------------------
*What is a False Positive?*

A false positive is a test result that incorrectly indicates the presence of a certain attribute. For instance, our code might indicate the presence
of a malignant tumor where, in reality, the tumor is benign.

*What is a False Negative?*

A false negative is a test result that incorrectly indicates the absence of a certain attribute. For instance, our code might indicate the status
of the tumor is benign where, in reality, it is malignant.

*What makes the measures of **Recall** and **Precision** different?*

Recall, or sensitivity, is the fraction of relevant data received over the total number of relevant data selected. Essentially, it is the fraction of true
positives over the overall number of positives. Precision is the fraction of relevant data over received data. So, it is the fraction of true positives
over the number of predicted positives (true positives / (true positives + false positives)).

Mean recall: 0.9562880911005326

Mean precision: 0.9565064856035251

These measures are slightly different because they evaluate a different fraction of data. However, the model generally creates a very similar ratio for
both measures. This means that the total true positives + false positives is approximately equal to the total positives.

######*What are sensible baselines for each of these measures?*

A sensible baseline for these measures is relatively more complex than the last baseline described. For these, 

######*How do the above results change with the **hyperparameter k**?*




