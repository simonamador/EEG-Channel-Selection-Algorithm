# EEG-Channel-Selection-Algorithm
*The following project was conducted as part of an on-going research on channel selection algorithms*
Database: https://physionet.org/content/eegmmidb/1.0.0/

## Purpose

The following project aimed to evaluate the influence PCA and sequential selection algorithms for channel selection in an electroencephalography (EEG) signal pre-processing on the accuracy of motion imagery classification for a multi-layer perceptron (MLP) and Convolutional Neural Network (CNN) classifiers.

## Preprocessing
Key points:
109 Subjects. Three are discarted (87, 91, 100) due to the sample size in the events from their registers.

Channels. 65

Frequency Rate. 160 Hz

14 Tasks each, time varies between 1 and 2 minutes. Tasks are as follows:

1.  Baseline, eyes open
2.  Baseline, eyes closed
3.  Task 1 (open and close left or right fist)
4.  Task 2 (imagine opening and closing left or right fist)
5.  Task 3 (open and close both fists or both feet)
6.  Task 4 (imagine opening and closing both fists or both feet)
7.  Task 1
8.  Task 2
9.  Task 3
10. Task 4
11. Task 1
12. Task 2
13. Task 3
14. Task 4

MNE library is used to extract, filter and segment data. Scikit-learn library is used for data normalization. The following preprocessing is conducted:
* Frequency filter 8-33 Hz (Mu & Beta waves)
* Segmentation
* Normalization

## Sequential Channel Selection
A sequential selection algorithm is done selecting channel sets of 1-6 channels.

## PCA
The PCA B4 method is applied to select channels which have the highest coefficients on the principal components which hold the most variance of the signal. Scikit-learn library is used for PCA

## Processing
Two deep learning classifiers are used, multi-layer perceptron (MLP) and convolutional neural network (CNN). TensorFlow library is used for classifiers.
