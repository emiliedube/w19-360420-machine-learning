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

Mean:

STD:

	*What is a sensible baseline against which we should compare our model's performance?*

Line 200 in DataSet.java details a method that prints a label indicating the frequency.

Analysis of Different Error Types
-------------------
	*What is a False Positive?*

A false positive is a test result that incorrectly indicates the presence of a certain attribute. For instance, our code might indicate the presence
of a malignant tumor where, in reality, the tumor is benign.

	*What is a False Negative?*

A false negative is a test result that incorrectly indicates the absence of a certain attribute. For instance, our code might indicate the status
of the tumor is benign where, in reality, it is malignant.

	*What makes the measures of **Recall** and **Precision** different?*

	*What are sensible baselines for each of these measures?*

	*How do the above results change with the **hyperparameter k**?*

Description of Results
--------------------

