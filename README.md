# CIFAR-10 Image Classification

## Overview
This project aims to classify images from the CIFAR-10 dataset using Artificial Neural Networks (ANN) and Convolutional Neural Networks (CNN). The performance of both models is compared based on their accuracy.

## Dataset
The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 different classes, with 6,000 images per class. The dataset is divided into 50,000 training images and 10,000 testing images. The classes include:
- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

##Model Example

```python
cnn=models.Sequential([
    #cnn
    layers.Conv2D(filters=32,activation='relu',kernel_size=(3,3),input_shape=(32,32,3)),
    layers.MaxPooling2D((2,2)),#Max pooling layer
    layers.Conv2D(filters=64,activation='relu',kernel_size=(3,3)),
    layers.MaxPooling2D((2,2)),

    #Dense Layers
    layers.Flatten(),
    layers.Dense(64,activation='relu'),
    layers.Dense(10,activation='softmax')
])
cnn.compile(optimizer='adam',loss='sparse_categorical_crossentropy',metrics=['accuracy'])
cnn.fit(X_train,y_train,epochs=10)
```


## Installation
To run this project, you need to have Python installed. Clone the repository and install the required packages:

```bash
git clone https://github.com/yourusername/Image_Classification_CIFAR10.git
cd Image_Classification_CIFAR10

