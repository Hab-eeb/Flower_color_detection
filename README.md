# Flower_color_detection

This repository is an implementation of some methods described in the paper "Automated color detection in orchids using color labels and deep learning" (https://doi.org/10.1371/journal.pone.0259036) as part of the Paper Review program organized by Zummit Africa. 

The method proposed in the paper is to detect Color of Flower (CF) and Color of Labellum (CL) in Orchids flower.

The repository includes:

Specifically Using Multiclass Classifier
	-For the Primary color Scheme
	
- Source code for building a multiclass color classifier using Deep Learning --> in the color_det_train file
	
	Basically, source code for each architecture used in the paper is the same, only need to change the type of pre-trained model and use different color schemes.
	
	In this repository, the attached code is for VGG16 by freezing only the first layer. 
	
	For the other architectures, just changes VGG16 into Xception, InceptionV3, Resnet50, and NasNet.
	
	For using multiclass classifier, train all the colors together in the same time. For example: to build CF1 classifier for primary color, train Green, Purple, Red, and Yellow together. Green, Purple, Red, and Yellow are used as the output class.
	
	For using different color schemes, just use different dataset: CF1 and CL1 for Color Scheme 1 and CF2 and CL2 for Color Scheme 2.


To use our code (redo our experiments):
1. Please setup the environment based on requirements.txt in the colab file.
2. The images for training, validation and testing should be put in different folders. 
3. The dataset (all of the images and the labels for training, validation and testing) can be downloaded from https://doi.org/10.7910/DVN/0HNECY. 
4. For using the images used in the method, please find the folder Color_Classifier. There are 2 folders: Multiple_Color and Primary_Color. Please use CF1, CF2, CL1 and CL2 folders for conducting experiments using various color schemes.
	
For Color of Flower (CF) in Primary Secondary Color using Color Scheme 2 and Color of Labellum (CL) in all scenarios, basically the codes are the same, only need to change the dataset for those scenarios.


# Refrences

https://github.com/d-harnoni 

https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0259036 

https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/0HNECY
