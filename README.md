# Hand Gesture Classification for Robotic Prosthesis Control

This repository contains code to implement hand gesture classification using LSTM networks. The study is based on the work by Kirill Yashuk, with modifications aimed at improving the network's performance and understanding its limitations when controlling a robotic prosthesis. This project was conducted under the 

## Summary

In this project, we have analyzed Kirill Yashuk's original code, which predicts hand gestures using an LSTM network. The purpose of this study is to control a robotic prosthesis by recognizing different hand movements. The original dataset was collected using a Myo armband, with four different hand gestures.

The main goals of this analysis were:
- **Dataset Analysis**: The sEMG signals were analyzed using Exploratory Data Analysis (EDA) to understand how well the network could predict hand gestures and to highlight any challenges posed by different muscle activations during various movements.
- **Training Modifications**: We modified the training process and evaluated the network using a new dataset obtained from the Ninapro database. The hyperparameters of the LSTM network were tuned to assess if different combinations could enhance performance.
- **Performance Comparison**: A cross-validation approach was used to compare the original dataset with the new dataset from Ninapro, which included similar movements to "rock-paper-scissors" and "ok." Due to the smaller size of the Ninapro dataset, the accuracy was slightly lower, but smoothing techniques (like linear envelope on rectified signals) helped achieve comparable results.
- **Gesture Addition**: Additional hand gestures from the Ninapro dataset were progressively added to the network, but the results showed a decrease in accuracy as more gestures were included, highlighting the limitations of the dataset and sensor placement.
- **Final Testing**: The network was tested on several other hand movement combinations to assess its capability to distinguish small differences in muscle activations. The results indicated limitations due to the small number of sensors and their inability to differentiate between the activation of specific muscles and movements of individual fingers.

Project's results are reported in detailed in the "LSTM Network for hand movement prediction" file.

## Implementation Details

- **K-fold Validation**: This code implements k-fold validation for better evaluation of the model.
- **Expanded Dataset**: We extended the model with additional hand gestures from the Ninapro dataset, which contains more complex and varied movements.
- **Training Process**: The code includes the option to adjust hyperparameters and train the network using modified datasets to evaluate the impact on accuracy.
  
