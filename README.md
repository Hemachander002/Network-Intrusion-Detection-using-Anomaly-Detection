(Enhanced version of this project will be uploaded within the first week of May, that includes model tracking , deployment and monitoring . im planning to transform this mini one into an end to end ML project Stay tuned for updates)

With the increasing volume of network traffic, detecting malicious activities (intrusions, attacks) is critical for maintaining system security,Traditional rule-based systems struggle 
to detect unknown or evolving attack patterns.This project aims to build an anomaly detection system to identify suspicious network traffic using machine learning.
The problem is treated as an anomaly detection task, where:
=> Normal traffic represents the majority class
=> Malicious traffic is rare and diverse

Models Used: Isolation Forest , Local Outlier Factor (LOF) , DBSCAN

Key Techniques :
1.Unsupervised Learning
2.Semi-supervised learning (training on normal data only)
3.Anomaly score threshold tuning
4.Model comparison and evaluation

Process :
1.Data preprocessing
2.Feature encoding and scaling
3.Trained Isolation Forest model by default first on the scaled data
4.Trained an another Isolation Forest model but with semi supervised approach
5.Trained DBSCAN model
7.Trained the LOF model
8.compared every models i have trained with confusion matrix and classification report

Results : 
LOF model performed well with the highest recall but the negative is it could trigger lot of false alarms 
Final Model: Isolation Forest (Semi-Supervised)
Recall (Attack Detection): ~95%
Precision: ~86%
Strong generalization on unseen test data

Confusion Matrix Comparison:

<img width="1259" height="570" alt="confusion matrix" src="https://github.com/user-attachments/assets/2865294f-de85-48f4-b099-0ca0fa358f77" />

t-SNE Visualization:
<img width="633" height="491" alt="Tsne" src="https://github.com/user-attachments/assets/26d917cb-edcf-4dd4-a920-5668c63dd154" />

=> Normal network behavior is highly structured and clustered
=> Anomalous traffic is scattered and diverse
=> Semi-supervised learning significantly improves anomaly detection
=> LOF, while sensitive, produces excessive false positives

Future Work : 
Planning to Deploy model using cloud platforms (Azure ML)
Real-time intrusion detection system
Model monitoring and drift detection



