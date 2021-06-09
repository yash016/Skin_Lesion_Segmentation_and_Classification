# Skin_Lesion_Segmentation_and_Classification

### This repository consists of Jupyter notebooks in which the task of segmenting the skin lesions as well as classifying them into 7 different categories is performed.

## Datasets Used:
### 1. Skin Lesion Segmentation: PH2 Database
PH² database contains a total of 200 dermoscopic images of melanocytic lesions, including 80 common nevi, 80 atypical nevi, and 40 melanomas with dimensions 768x560 pixels.

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/PH2_image_sample.png)

**Link for download**: [PH2 Database](https://www.fc.up.pt/addi/ph2%20database.html) 

### 2. Skin Lesion Classification: HAM10000 Dataset
HAM10000 dataset consists of 10015 dermatoscopic images which can serve as a training set for academic machine learning purposes. The dimension of images in this dataset is 600x450 pixels.

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Lesion_Classification.png)

**Link for download**: [HAM10000 Dataset](https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000)




## Models:

### 1. Skin Lesion Segmentation:
#### 1. Fully Convolutional Network(FCN):
Fully Convolutional Networks, or FCNs, are an architecture used mainly for semantic segmentation. They employ solely locally connected layers, such as **convolution**, **pooling** and **up sampling**. Avoiding the use of dense layers means less parameters (making the networks faster to train). It also means an FCN can work for variable image sizes given all connections are local

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/FCN.png)

**Research Paper**: [Fully Convolutional Networks for Semantic Segmentation](https://arxiv.org/pdf/1411.4038.pdf)

#### 2. UNet:
U-Net is an architecture for Biomedical image segmentation. It consists of a contracting path and an expansive path, which gives it the u-shaped architecture. The contracting path is a typical convolutional network that consists of repeated application of convolutions, each followed by a rectified linear unit (ReLU) and a max pooling operation. During the contraction, the spatial information is reduced while feature information is increased. The expansive pathway combines the feature and spatial information through a sequence of up-convolutions and concatenations with high-resolution features from the contracting path.

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/UNet.png)

**Research Paper**: [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/pdf/1505.04597v1.pdf)

### 2. Skin Lesion Classification:
#### 1. Convolutional Neural Network
![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Classification_model.png)




## Results:

### 1. Skin Lesion Segmentation:
#### 1. Fully Convolutional Network(FCN):

* **On Train Set**:

| Parameters | Values |
|----------- |------- |
| IOU:       | 95.06  |
| Dice Coeff:| 77.43  |
| Precision: | 95.67  |
| Recall:    | 93.37  |
| Accuracy:  | 96.57  |
| Loss:      | 4.94  |


* **On Test Set**:

| Parameters | Values |
|----------- |------- |
| IOU:       | 94.08  |
| Dice Coeff:| 76.05  |
| Precision: | 91.94  |
| Recall:    | 92.89  |
| Accuracy:  | 95.22  |
| Loss:      | 5.92  |

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Lesion_Segmentation_Result_FCN.png)

#### 2. UNet:

* **On Train Set**:

| Parameters | Values |
|----------- |------- |
| IOU:       | 96.36  |
| Dice Coeff:| 90.89  |
| Precision: | 92.81  |
| Recall:    | 95.57  |
| Accuracy:  | 96.24  |
| Loss:      | 3.64  |


* **On Test Set**:

| Parameters | Values |
|----------- |------- |
| IOU:       | 94.87  |
| Dice Coeff:| 88.57  |
| Precision: | 89.13  |
| Recall:    | 94.86  |
| Accuracy:  | 94.88  |
| Loss:      | 5.13  |

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Lesion_Segmentation_Result_UNet.png)

### 2. Skin Lesion Classification:

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Lesion_Classification_accuracy.png)   ![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Lesion_Classification_Loss.png)

![alt text](https://github.com/yash016/Skin_Lesion_Segmentation_and_Classification/blob/main/Images/Skin_Classifications.png)
