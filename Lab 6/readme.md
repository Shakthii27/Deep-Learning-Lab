# Experiment 6 – RNN, LSTM and GRU for Sequence Learning and Video Understanding

## Overview

This experiment provides an end-to-end study of recurrent neural networks for sequence learning and video understanding. The main objective is to understand how sequential data can be represented, processed, and classified using Vanilla RNN, LSTM, and GRU architectures. The experiment also covers Backpropagation Through Time (BPTT), temporal dependencies, model convergence, and the limitations of conventional RNNs.

## Dataset

The primary dataset used is the **UCI Human Activity Recognition (HAR) dataset**. It contains smartphone sensor measurements corresponding to six activities: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, and LAYING. The raw inertial signals were converted into temporal sequences of 128 time steps and 9 sensor channels.

## Experiments Performed

The experiment includes preprocessing and normalization of the sensor data, temporal visualization, and a manual numerical implementation of an RNN hidden-state calculation. Vanilla RNN, LSTM, and GRU models were then trained and evaluated using accuracy, precision, recall, Macro F1-score, confusion matrices, parameter count, and training time.

The obtained results were:

| Model | Accuracy | Macro F1 |
|---|---:|---:|
| RNN | 84.00% | 83.87% |
| LSTM | 94.67% | 94.68% |
| GRU | 95.33% | 95.33% |

A sequence-length experiment was also performed using sequence lengths of 32, 64, and 128 to study the effect of temporal context.

## Video Understanding

The experiment was extended to video understanding using a CNN–LSTM pipeline. A pretrained MobileNetV2 model was used to extract spatial features from video frames, which were then processed as temporal sequences by an LSTM.

## Sequence-to-Sequence Learning

Finally, an Encoder–Decoder LSTM was implemented for a synthetic sequence-reversal task. The model achieved 100% token accuracy and 100% sequence accuracy on the validation set using teacher forcing.

## Repository

The complete source code, notebooks, outputs, and experiment files are available here:

**GitHub:**  
https://github.com/Shakthii27/Deep-Learning-Lab/tree/main/Lab%206
