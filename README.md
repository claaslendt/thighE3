# Thigh-EEE

This repository is dedicated to the research project 'Estimation of activity induced energy expenditure using thigh-worn accelerometry and machine learning approaches'. This project was funded by the Internal Research Funds of the German Sport  University Cologne, grant agreement number L-11-10011-267-121010. Claas  Lendt is further supported by a fellowship of the German Academic Exchange  Service (DAAD).

*All code and data will be added at a later stage of the project.*



## Short background

Accurate assessment of activity-induced energy expenditure (AEE) is required to investigate its relationship with health outcomes and to potentially enable individualised energy balance feedback systems. While accurate measurement methods exist in the laboratory (e.g. doubly labelled water or indirect calorimetry), the challenge is to provide accurate estimates of AEE in free-living conditions. This is typically done using portable and unobtrusive systems such as accelerometry, but these systems are currently not accurate enough for research and clinical applications. The proposed research project therefore aims to train and validate a machine learning model to estimate AEE using raw acceleration data collected from the thigh. Activity classification and stride segmentation algorithms will be used as additional model inputs.



## Our approach

To support efficient and robust training of the machine learning model, a diverse population sample will be recruited. All sample participants will undergo a standardised activity protocol in the laboratory while AEE will be measured using indirect calorimetry. The raw triaxial acceleration of the thigh will be measured and used for subsequent modelling. Activity classification and stride segmentation will be performed on the raw acceleration data using existing algorithmic approaches and subsequently used as model inputs. Model performance will be evaluated against indirect calorimetry and previous regression models.

In collaboration with the AUT Human Potential Centre, we will implement existing and validated activity classification algorithms. In addition, we plan to merge prospective, co-existing datasets to enhance our ability to train and test the modelling approach. Based on previous research using activity classification and stride segmentation, we expect the novel modelling approach to perform with greater accuracy compared to existing thigh-based estimation models as well as other wearable systems (such as a commercial smartwatch).



![Fig1](https://github.com/claaslendt/thighE3/blob/main/figures/Fig1.jpg)



## Progress of the project :rocket:

(Last update: 2024-05-06)

We have made significant progress since the start of the project. We have collected all our data in the lab.  We have managed to pool several existing activity classification datasets (based on GSU and AUT data) to train our deep learning classification algorithm. And in the last few weeks, we have been able to build a proof-of-concept pipeline that will undergo final validation using a hold-out sample.

**A quick overview on our progress so far**

- [x] **Data collection** at GSU Cologne.
- [x] **Cleaning and pre-processing** of the collected data.
- [x] **Training of a CNN-LSTM activity classification model** using a pooled dataset of laboratory and free-living data (n = 69) with  more than 100.000 data points across a range of different physical activities.
- [x] **Development and validation of the activity-specific stride segmentation approach** for walking, running and cycling.
  
- [x] **Development of several EE estimation approaches**
  - [x] generic approaches (using ENMO and MAD)
  - [x] activity-specific approaches
  - [x] stride-specific approaches
  - [x] activity- AND stride-specific approaches
- [ ] **Final analysis and validation using the hold-out test set**



## Impressions

We are looking forward to share our final approach, the validation results and methods in the near future. Stay tuned!

Meanwhile, you can find a few impressions below.



**Figure 1**. Example of stride segmentation for walking data.

![StrideSegmentationWalking](https://github.com/claaslendt/thighE3/blob/main/figures/StrideSegmentationWalking.png)



**Figure 2**. Preliminary results for the validation data using an activity- and stride-specific LSTM approach.

![Validation_EEStride](https://github.com/claaslendt/thighE3/blob/main/figures/Validation_EEStride.png)



**Figure 3**. Confusion matrix for the activity classification model for the validation set.

![confmat_classifier](https://github.com/claaslendt/thighE3/blob/main/figures/confmat_classifier.png)
