# Malaria Detection

[![dataset](https://img.shields.io/badge/Kaggle-Dataset-blue)](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria) 

*Malaria is a mosquito-borne infectious disease that affects humans and other animals. Malaria causes symptoms that typically include fever, tiredness, vomiting, and headaches. In severe cases it can cause yellow skin, seizures, coma, or death. Symptoms usually begin ten to fifteen days after being bitten by an infected mosquito.*

## Objective

The current standard method for malaria diagnosis in the field is light microscopy of blood films. About 170 million blood films are examined every year for malaria, which involves manual counting of parasites. To improve the accuracy and speed of this testing, the project aims to distinguish Malaria infected human blood cells from the normal ones.

## Dataset 

Malaria Cell Images Dataset is used for the training and testing of the model. The dataset is available in Kaggle in the website: [https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria](https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria). However, this Dataset is taken from the official [NIH Website](https://ceb.nlm.nih.gov/repositories/malaria-datasets/).

### Contents

The dataset contains 2 folders

* Parasitized
<div align="center">
<table>
  <tr>
    <td width="50%"> <img src = "./Images/Infected_1.png" width="200%"><br>(a) </td>
    <td width="50%"> <img src = "./Images/Infected_2.png" width="200%"><br>(b) </td>
  </tr>
</table>
<p>(a), (b) Sample images of parasitized human blood cells.</p>
</div>
<br><br>

* Uninfected
<div align="center">
<table>
  <tr>
    <td width="50%"> <img src = "./Images/Uninfected_1.png" width="100%"><br>(a) </td>
    <td width="50%"> <img src = "./Images/Uninfected_2.png" width="100%"><br>(b) </td>
  </tr>
</table>
<p>(a), (b) Sample images of normal uninfected human blood cells.</p>
</div>
<br><br>

And a total of 27,558 images of cells from different blood films for analysing and predicting Image Cells that contain Malaria parasites or not.

**Note:** The image resolution in the images is not uniform.

## Methodology

### VGG19
VGG-19 is a 19-layer convolutional neural network. The ImageNet database contains a pretrained version of the network that has been trained on more than a million images. The pretrained network can categorise images into 1000 different item categories, including several animals, a keyboard, a mouse, and a pencil. The VGG19 model has been used in the project as a feature extractor.

<div align="center">
<img src = "./Images/VGG19.jpg" width="100%">
<p>VGG19 Architecture </p>
</div>

### Custom Architecture
On top of VGG19 architecture, a custom architecture is added to enhance the performance and implement transfer learning in this specific case.

<div align="center">
<img src = "./Images/Custom_model.png" width="100%">
<p>VGG19 Architecture </p>
</div>

## Results

The model was trained upon the Malaria Cells Image Dataset for 50 epochs. It achieved a training loss of 0.0433 and an accuracy of 0.9904 along with validation loss and validation accuracy of 0.2561 and 0.9104 respectively.

<div align="center">
<table>
  <tr>
    <td width="50%"> <img src = "./Images/output.png" width="100%"><br>(a) </td>
    <td width="50%"> <img src = "./Images/output2.png" width="100%"><br>(b) </td>
  </tr>
</table>
<p>(a), (b) The graphs portray the training and validation loss and accuract respectively.</p>
</div>
<br><br>