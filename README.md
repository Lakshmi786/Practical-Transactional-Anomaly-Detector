# Practical-Transactional-Anomaly-Detector



# Problem and Requirements:
### In finance Such as Banking , Ecommerce some users perform illegal transactions in the database and those transactions leave records in database. How ever this database is mostly composed of non criminal transactions from the people who comply with the rules of the system they are part of.
# Goal: 
###To identify this Fraudulant Transactions by means of running our Database through Anamoly detection system.


# What is Anomaly?
### Anomaly refers to an observation or data point that is significantly different from the rest of the dataset. Anomalies are also called outliers because they are data points that lie outside the normal range or distribution of data.

### Anomalies can be caused by a variety of factors, including measurement errors, data entry errors, or simply representing rare but legitimate data patterns. However, anomalies can also be indicative of fraudulent activity, system errors, or other issues that require further investigation.

### Detecting anomalies is an important task in machine learning and data analysis, as it can help identify and prevent potential problems or errors. Machine learning techniques such as clustering, classification, and anomaly detection algorithms can be used to identify and flag unusual or unexpected patterns in data, which can then be investigated further to determine the cause and appropriate course of action.


# Data:
### Paysim synthetic dataset of mobile money transactions. Each step represents an hour of simulation. This dataset is scaled down 1/4 of the original dataset which is presented in the paper "PaySim: A financial mobile money simulator for fraud detection".

 


# Isolation Forest: Intuition
### Isolation Forest assigns an anomaly score to data points based on how easy they are to separate from the rest of the data. The easier a data point is isolated from the majority of the data, the more likely it is to be an anomaly. But how does the model determine whether a point is ‘easier’ to isolate in practice? Simply put, the model tries to isolate points by asking random questions of the following form:

Is feature x larger or smaller than threshold y?

Both feature x and the threshold y are chosen randomly. Given enough random questions, eventually every unique data point will be isolated. Isolation Forest considers points that require more such questions as harder to isolate and thus more likely to be anomalies. To get an intuition for why this works, consider the following two processes of isolation for different data points. Let’s first look at a point that could be considered an anomaly in the sense that there are not many other points similar to it.



To Run the model refer the notebook  [Object_Detection_Detecto_car.ipynb](Object_Detection_Detecto_car.ipynb)

