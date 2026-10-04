# AI-Driven Threat Detection for Secure Aircraft Communication Networks

## Overview

This research project investigates whether machine learning can detect cyber threats in aircraft communication networks by identifying abnormal traffic patterns.

As aviation systems become increasingly dependent on digital communication networks, new cybersecurity risks can emerge. Malicious traffic such as spoofed messages, flooding, false telemetry, and denial-of-service attacks could potentially disrupt or compromise flight-critical systems.

This project explores the use of **Artificial Intelligence (AI)** and **Machine Learning (ML)** to distinguish normal aircraft communication traffic from simulated malicious traffic.

> **Note:** This project uses a simulated aircraft communication dataset and is intended for academic research and experimentation. It does not use real aircraft network data.

## Research Question

**Can machine learning detect cyber threats in aircraft communication networks by identifying abnormal traffic patterns?**

## Objective

The objective of this research is to identify suspicious patterns in aircraft communication networks using a machine learning-based detection approach.

## Hypothesis

A **Random Forest** machine learning model can effectively identify abnormal aircraft communication traffic and distinguish it from normal communication patterns.

## Dataset

A simulated aircraft communication dataset was used to represent normal and malicious network traffic.

The dataset contains features related to aircraft communication behavior, including:

* Packet size
* Transmission frequency
* Source node
* Destination node
* Protocol type
* Delay
* Traffic label

The simulated traffic includes both:

* **Normal aircraft communication**
* **Malicious/injected traffic**

The project considers attack scenarios such as:

* Spoofed control messages
* Packet flooding
* False telemetry injection
* Denial-of-service behavior
* Replay and fuzzing behavior

## Methodology

### 1. Data Collection

A simulated aircraft communication dataset was generated to represent normal and malicious network traffic.

### 2. Data Preprocessing

The data was prepared for machine learning by:

* Cleaning the dataset
* Encoding categorical features
* Labeling normal and malicious traffic
* Selecting relevant communication features

### 3. Model Training

A **Random Forest classifier** was used as the primary machine learning model.

The model was configured with:

* **100 decision trees**
* `n_estimators = 100`
* Gini impurity
* 80/20 train-test split
* Stratified data splitting

Random Forest was selected because it performs well on tabular classification problems and provides feature importance information that can help interpret the model's decisions.

### 4. Evaluation

The model was evaluated using:

* Accuracy
* Precision
* Recall
* Confusion matrix
* Feature importance

## Results

The trained Random Forest model achieved an overall accuracy of approximately **85%** on the test data.

Key results included:

| Metric                 |                         Result |
| ---------------------- | -----------------------------: |
| Overall Accuracy       |                            85% |
| Attack Precision       |                            92% |
| Normal Recall          |                            97% |
| Attack Recall          |                            60% |
| Most Important Feature | Transmission Frequency (30.8%) |

The results indicate that the model was particularly effective at recognizing normal traffic and achieved high precision when identifying malicious traffic. However, the lower attack recall demonstrates that some malicious traffic was not detected, highlighting an important area for improvement.

## Key Finding

**Transmission frequency** was the most influential feature in the Random Forest model, suggesting that abnormal communication frequency may provide a useful signal for distinguishing malicious traffic from normal aircraft communication behavior.


## Technologies

* Python
* Pandas
* Scikit-learn
* Random Forest
* Google Colab
* Jupyter Notebook
* Microsoft Excel
* Data visualization

## Limitations

This research uses a **simulated dataset**, so the results may not fully represent the complexity of real aircraft communication networks.

The model also produced a lower recall for malicious traffic, meaning some attacks were not detected. Improving the detection of malicious traffic is therefore an important area for future development.

## Future Work

Future development could include:

* Testing on larger and more realistic datasets
* Incorporating real-world aviation cybersecurity datasets where available
* Comparing Random Forest with other ML and deep learning models
* Detecting specific attack categories individually
* Developing real-time anomaly detection
* Testing additional network and communication features
* Improving detection of previously unseen attack patterns

## Research Context

This project was developed as an academic machine learning and cybersecurity research project exploring the application of AI to aviation cybersecurity.

## Author

**Layan**

Computer Science Student
AI / Machine Learning | Cybersecurity | Software Development

