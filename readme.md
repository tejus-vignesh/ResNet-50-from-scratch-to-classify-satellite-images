# ResNet-50 from scratch to classify satellite images
"This repository contains code to build and train a ResNet-50 architecture model from scratch for land use and land cover classification using Sentinel-2 satellite images. 

I compared the model's performance metrics on original 64x64 pixel images and up-scaled (Bilinear Interpolation) 224x224 pixel images."

In my experiments the model was trained on a single NVIDIA P100 GPU.

## Dependencies
- pip install seaborn
- pip install tensorflow
- pip install scikit-learn

## Dataset
The dataset used is the [EuroSAT dataset](https://github.com/phelber/eurosat), which is a dataset of satellite images of europe. The dataset contains 27,000 labeled images of size 64x64 pixels. The images are divided into 10 classes, with ~2,700 images per class.

## Data preprocessing
The original 64x64 pixel images underwent preprocessing, which involved random horizontal flipping, shearing, and zooming. This preprocessing was also applied to the images after up-scaling them to 224x224 pixels using Bilinear Interpolation. Up-scaling allowed comparison of the model's performance on both original and up-scaled images.

## Training the model
To train the model with the hyperparameters specified in the code, execute the cells on an instance equipped with a P100 GPU. The trained model will be saved in the current directory.

Before running the cells, ensure that you modify the `file_path` variable to point to the location where the dataset is stored.

The hyperparameters of the model can be adjusted to experiment with different configurations, depending on the available hardware.