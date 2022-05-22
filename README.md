# Pneumonia-Detection-from-X-Ray-Images🩺
### Detection of pneumonia from X Ray images using Pytorch 

The architectures used are ResNet9, ResNet18 and other custom CNN models. The final model selected for use is ResNet18. Hyperparameters have been selected using optuna. Evaluation has been done using k fold cross validation for the final ResNet model. Ensembling used for 5 ResNet models trained on 5 different fold of the training Dataset

## Dataset 📂

- The dataset has been taken from Kaggle [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia) dataset which consists of Chest X-ray images (anterior-posterior) selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. 
- The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal)

## Notebook 📙

- There are 3 notebooks, each containing different models
  - [pneumonia-prediction-ResNet9.ipynb](https://github.com/rigvedrs/Pneumonia-Detection-from-X-Ray-Images/blob/main/pneumonia-x-ray-ResNet9.ipynb)
  - [pneumonia-prediction-deepL.ipynb](https://github.com/rigvedrs/Pneumonia-Detection-from-X-Ray-Images/blob/main/pneumonia-prediction-deepL.ipynb)
  - [pneumonia-prediction-resnet18.ipynb](https://github.com/rigvedrs/Pneumonia-Detection-from-X-Ray-Images/blob/main/pneumonia-resnet18.ipynb)

## Ideas 💭


