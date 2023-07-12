# Melanoma Detection
> Detect Melanoma based on the images given.

## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Recommendationss](#recommendations)

<!-- You can include any other section that is pertinent to your problem -->

## General Information

#### Problem statement
	To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
	
        The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). 


## Conclusions

#### We came up with 3 Models

| Models | Train Accuracy | Test Accuracy | Epochs |
| --- | --- | --- |--- |
|  Model1(Base Architecture Model) | 70.1 | 51.6 | 20 |
|  Model2(Data Augmentation/Dropouts|  52.5|  52.5 | 20 |
|  Model3(Class rebalance/Batch Norm)|  72  |  69  | 50 |


- Model1(Base model) behaved poorly and overfitted on the Validation set. This indicated that the model was simply memorizing the training set and failing to recognize any genuine patterns.

- Model2(Data Augmentation/Dropouts)Data Augmentation and dropouts helped big time to overcome the issue of overfitting. Thought accuracy was low model learnt and behaved consistently on the Validation sets

- Model3(Class rebalance/Batch Norm) - Class rebalance and Batch norm helped further increased the accuracy to 72% on the training set and 69% on Vaidation set which showed a lot of improvements from Model2. However, we observed the accuracy being oscilating during 50 epochs on validation set. This was happening probably due Batch normaliation using smaller batch size.

## Recommendations:--
#### To increase the accuracy following can be tried:-
- Increase the batch size for batch  normalization . This will certainly reduce the noise.
- Try Group normaliation to make model stable
- Adjust the momentum of Batch Normaliation

