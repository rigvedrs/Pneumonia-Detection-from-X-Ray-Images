# Pneumonia-Detection-from-X-Ray-Images🩺
### Detection of pneumonia from X Ray images using Pytorch 

The architectures used are ResNet9, ResNet18 and other custom CNN models. The final model selected for use is ResNet18. Hyperparameters have been selected using optuna. Evaluation has been done using k fold cross validation for the final ResNet model. Ensembling used for 5 ResNet models trained on 5 different fold of the training Dataset

## Dataset 📂

- The dataset has been taken from Kaggle [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia) dataset which consists of Chest X-ray images (anterior-posterior) selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. 
- The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal)

## Pneumonia Images (grayscaled) 🔬


![pneumonia images](/assets/pneumonia.png)


## Normal Images (grayscaled) 🔬


![Normal images](/assets/normal.png)


## Pneumonia vs Normal Images 📊

![Pneumonia vs Normal](/assets/pneumoniavsnormal.png)

## Notebook 📙

- There are 3 notebooks, each containing different models
  - [pneumonia-prediction-ResNet9.ipynb](https://github.com/rigvedrs/Pneumonia-Detection-from-X-Ray-Images/blob/917e8f2691dfe7212ddf21ec2f70a4ab353543c2/pneumonia-prediction-ResNet9.ipynb)
  - [pneumonia-prediction-deepL.ipynb](https://github.com/rigvedrs/Pneumonia-Detection-from-X-Ray-Images/blob/917e8f2691dfe7212ddf21ec2f70a4ab353543c2/pneumonia-prediction-deepL.ipynb)
  - [pneumonia-prediction-resnet18.ipynb](https://github.com/rigvedrs/Pneumonia-Detection-from-X-Ray-Images/blob/917e8f2691dfe7212ddf21ec2f70a4ab353543c2/pneumonia-prediction-resnet18.ipynb)

## Ideas and Techniques Implemented 💭

- Basic Data preprocessing involving:
  -  Understanding data 
  -  Transforming data 
     - Applying Random Rotations  
     - Normalizing RGB values
     - Resizing
- Models used:
  - ResNet9
  - ResNet18
  - Other custom CNN models
- Weight decay
- Automatized Hyperparameter search using optuna
- K Fold Cross Validation
- Ensembling, by dividing the training data into 5 folds and training 5 ResNet18 models seperately with the seperate folds of data and using the average of their outputs as the final prediction.

## Losses and accuracies recorded 📈

### ResNet9:

![ResNet9](/assets/ResNet9.png)

### Custom CNN model:

![Custom](/assets/custom.png)

### ResNet18:

![ResNet18](/assets/ResNet18.png)


## Final Outputs:

![output](/assets/output.png)

## Accuracies Recorded: 🎓
<h4>
<ul>
  <li>ResNet9:
    <ul>
      <li>Training 56%</li>
      <li>Testing 51%</li>
    </ul>
  </li>
  </ul>
  <ul>
  <li>Custom CNN:
    <ul>
      <li>Training 97%</li>
      <li>Testing 84%</li>
    </ul>
  </li>
  <li>ResNet18:
    <ul>
      <li>Training 96%</li>
      <li>Testing 91%</li>
      <li>After ensembling 94%</li>
    </ul>
  </li>
</ul>
</h4>
