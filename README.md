# Detecting Human Posture Using a Convolutional Deep Neural Network¶


## Experiment Objective
Create a deep learning neural network that can detect human posture from silhouettes. This dataset contains 1200 images for each of the following postures:

1. Sitting
2. Standing
3. Bending
4. Lying

The dataset comes with each image resized to the dimension of 512x512 px. Images have not been labeled directly but have been placed in respective class folders based off the posture in the image.

## Data Collection and Preprocessing
Source: https://ieee-dataport.org/open-access/silhouettes-human-posture-recognition License: Creative Commons Attribution Details on the Terms of Use for this License: https://creativecommons.org/licenses/by/4.0/ and https://creativecommons.org/licenses/by/4.0/legalcode

About IEEE Dataport

"IEEE developed IEEE DataPort to provide significant benefits to researchers, data analysts, and the global technical community. The platform offers free uploads of any dataset up to 2TB for those that need to retain and manage their valuable research data and it offers free access to the datasets on IEEE DataPort. The platform currently has over 425,000 global users and over 1,500 datasets and continues to provide value to researchers around the globe."

Authors of Dataset: Abhishek Kumar (Indian Institute of Information Technology Kottayam) and Ebin Deni Raj (Indian Institute of Information Technology Kottayam)

Note: Many functions used in the code below were repurposed from: https://github.com/rasbt/python-machine-learning-book-3rd-edition Copyright (c) 2019 Sebastian Raschka

## Results
Using epochs=15, and batch size=32, we were able to achieve a 91.5% accuracy on our validation data with our custom estimator. Therefore, our CNN was able to successfully classify human silhouette photos with 91.5% accuracy.

With the same parameters and data, we re-ran our model using fit instead of the estimator and found very similar results with validation accuracy of 91% and a training accuracy of 90%.

After about epoch 15, overfitting begins to occur. The graph of accuracy above extrapolated further would clearly indicate overfitting, so we stop at 15.

Overall, our model performs well, but further tuning of the hyperparameters in each layer of the CNN should help to increase accuracy on new data.
