# ECG-Heartbeat-Data

Source of data: https://www.kaggle.com/shayanfazeli/heartbeat

Context

ECG Heartbeat Categorization Dataset


This dataset is composed of two collections of heartbeat signals derived from two famous datasets in heartbeat classification, the MIT-BIH Arrhythmia Dataset and The PTB Diagnostic ECG Database. The number of samples in both collections is large enough for training a deep neural network.

This dataset has been used in exploring heartbeat classification using deep neural network architectures, and observing some of the capabilities of transfer learning on it. The signals correspond to electrocardiogram (ECG) shapes of heartbeats for the normal case and the cases affected by different arrhythmias and myocardial infarction. These signals are preprocessed and segmented, with each segment corresponding to a heartbeat.


Content of Data
Arrhythmia Dataset
Number of Samples: 109446
Number of Categories: 5
Sampling Frequency: 125Hz
Data Source: Physionet's MIT-BIH Arrhythmia Dataset
Classes: ['N': 0, 'S': 1, 'V': 2, 'F': 3, 'Q': 4]
The PTB Diagnostic ECG Database
Number of Samples: 14552
Number of Categories: 2
Sampling Frequency: 125Hz
Data Source: Physionet's PTB Diagnostic Database
Remark: All the samples are cropped, downsampled and padded with zeroes if necessary to the fixed dimension of 188.


Acknowledgements
Mohammad Kachuee, Shayan Fazeli, and Majid Sarrafzadeh. "ECG Heartbeat Classification: A Deep Transferable Representation." arXiv preprint arXiv:1805.00794 (2018).

Code for this repo

The initial notebook (_Baseline) is using simple Machine Learning techniques to try to predict the data and establish a baseline of their perofmrance.  4 Models were used:
- SVM
- Extra Tress Classifier
- Logistic Regression
- Gradient Boosting Classifier (as recommended by Auto ML)

For the PTB dataset the classifiers did really well and its hard to imagine that a deep learning model can outperform them without taking a significant performance hit for a neglibile improvement in prediction results.  For the MIT multi-classification dataset, a deep learning model could probably improve the performance but the baseline results were quite good for the majority of the classes.
