Solution for Quiz-2
CSCE 590-1: From Data to Decisions with Open Data: A Practical Introduction to AI
Prof. Biplav Srivastava, Spring 2021
Student: Avineet Kumar Singh
Question 1: Classification
German credit dataset is a popular dataset in ML. It can be found at in multiple formats at (.csv,
.arff):
https://www.openml.org/t/31
https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data)
1(a): Download the data and pre-process in any way necessary. How many data items and
features does it have? What are their types? [10 points]
Solution:
Number of data items: 1000, Features: 21
Type of data:
 

Numeric features: 7
Nominal features: 14 
Data Preprocessing is performed using two methods:
1) Using Sklearn (giving numbers to categories/label encoding the data)
2) Using Pandas(one hot encoding)
 

1(b) Perform classification on the class label with at least two methods.
Present model accuracy, recall and F1 statistics. If possible, print model structure.
Solution:
Code: 
Classifier 1: SVM
 
Classifier 2: Random Forest
 





Question 2: Clustering
Cluster the data with any method without giving the number of classes. Now compare the
clusters with the classes. Find the homogeneity, completeness, and v-score metrics.
Solution:
Code:
Clustering Method: DBSCAN
Identified clusters: [-1  0  1  2  3  4  5]
Clustering Performance Evaluations:
 

Question 3: Bonus:
The dataset has attributes for age and personal_status. What is the distribution of class with
respect to these attributes? Is there a age or personal_status group that can perceive bias?
Feel free to pre-process data to gain insights – e.g., binning for age.
Solution:
Code:
distribution of ‘personal_status’ based on ‘class’ label:
 
distribution of ‘age’ based on ‘class’ label(After Categorizing age):
 
Plotting ‘age’ and ‘personal_status’ groups based on ‘class’ label

 
Study of Biasness in dataset ( as per age and personal_status group )
Based on the above tables and figures following biasness could be identified:
1) Categories for female customers are low as male customers are divided into more categories as per personal status. Even if the dataset is small, the categories for personal status should be balanced among both the genders.
2) As per personal status, the ratio of good credit risks to bad credit risks customers is higher for  ‘male-single’ customers. It means there is a slight biasness in considering marital status for determining good and bad credit risks.
3) As per age category, the ratio of good credit risks to bad credit risks customers is higher for  age category of ’33-55’. People in this category are considered more stable which may not be true. 
4) As per the plot, for ‘female div/dep/mar’ the number of bad credit risks increase as compared to good credit risks after the age of 35(approx.), which is not prevalent in other categories at that age.
