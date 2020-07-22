# Personalized-Cancer-Diagnosis

The workflow is as follows

* A molecular pathologist selects a list of genetic variations of interest that he/she want to analyze
* The molecular pathologist searches for evidence in the medical literature that somehow are relevant to the genetic variations of interest
* Finally this molecular pathologist spends a huge amount of time analyzing the evidence related to each of the variations to classify them.

Our goal here is to replace step 3 by a machine learning model. The molecular pathologist will still have to decide which variations are of interest, and also collect the relevant evidence for them. But the last step, which is also the most time consuming, will be fully automated.

## Dataset

We have two data files: 
1. One conatins the information about the genetic mutations 
2. Other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.

#### Both these data files are have a common column called ID
* Data file's information:

  * training_variants (ID , Gene, Variations, Class)
  * training_text (ID, Text)

## Mapping the real-world problem to an ML problem
Type of Machine Learning Problem

       **There are nine different classes a genetic mutation can be classified into => Multi class classification problem**
       
## Performance Metrics
Metric(s):

* Multi class log-loss
* Confusion matrix

<h3>Machine Learing Objectives and Constraints</h3>
  
Objective: Predict the probability of each data-point belonging to each of the nine classes.

Constraints:

* Interpretability 
* Class probabilities are needed. 
* Penalize the errors in class probabilites => Metric is Log-loss. 
* No Latency constraints.
