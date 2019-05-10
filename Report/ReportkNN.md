kNN Machine Learning Error Analysis Report
===========

##### Emilie Dub� and Aidan Zentner
##### Professors Sameer Bhatnager and Jean-Fran�ois Bri�re

##### Intro to Computer Programming in Engineering and Science

##### Section 02

##### May 14 2019

Confidence in Model
-------------------
*Why do we get a different accuracy each time we run the classification model?*

In DataSet.java, lines 148 to 150 explain why the accuracy each time the classification model is run is different. 
In java, the class method '.shuffle' from the 'Collections' class accesses different elements randomly from a given String.
Thus, each time we cut the data set, we work with a different section of data. This affects the accuracy of the overall results.