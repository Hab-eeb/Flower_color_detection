# Orchids-Color-Detection

This repository is an implementation of some methods described in the paper "Automated color detection in orchids using color labels and deep learning" (https://doi.org/10.1371/journal.pone.0259036). The method was proposed to detect Color of Flower (CF) and Color of Labellum (CL) in Orchids flower.

1. Using Multiclass Classifier
	- Primary color
	- Primary and Secondary color
3. Using Binary Classifier
	- Primary color
	- Primary and Secondary color

The repository includes:
- Source code for building color classifiers using Deep Learning --> in the folder "multiclass"
	
	Basically, source code for each architecture used in the paper is the same, only need to change the type of pre-trained model and use different color schemes.
	
	In this repository, the attached code is for Xception by freezing only the first layer. 
	
	For the other architectures, just changes Xception into VGG16, InceptionV3, Resnet50, and NasNet.
	
	For using multiclass classifier, train all the colors together in the same time. For example: to build CF1 classifier for primary color, train Green, Purple, Red, and Yellow together. Green, Purple, Red, and Yellow are used as the output class.
	
	For using binary classifier, train each color separately. For example: to build CF1 classifier for primary color, train Green, Purple, Red, and Yellow separately (Please see "binary" folder). Green Classifier will output Green and Non-Green class, Purple will output Purple and Non-Purple class, etc.
	
	For using different color schemes, just use different dataset: CF1 and CL1 for Color Scheme 1 and CF2 and CL2 for Color Scheme 2.
		
- Source codes for determining the color (output the color label) --> in the folder "color label"
	
	The code is used to assign the color for Combined-Binary Classifier. 
	
	As mentioned in the paper, we proposed 2 methods. First is using one-versus-the-rest (method 1) and second is using maximum probability (method 2).
	
	Besides that, we also need to assign the color label for Ensemble Classifier (combining a multi-class and combined-binary classifier).
	
	For Ensemble Classifier, we also proposed 2 methods. First is using MLTC (Most likely true color). Second is using MLCR (Most likely color ratio).
	
	We don't need to assign color label in Multiclass Classifier because the classifier is directly giving us the color label.
- Results --> in the folder "results"

	Contains the results for all the experiments.

To use our code (redo our experiments):
1. Please setup the environment based on requirements.txt.
2. The images for training, validation and testing should be put in different folders. 
3. The dataset (all of the images and the labels for training, validation and testing) can be downloaded from https://doi.org/10.7910/DVN/0HNECY. 
4. For using the images used in the method, please find the folder Color_Classifier. There are 2 folders: Multiple_Color and Primary_Color. Please use CF1, CF2, CL1 and CL2 folders for conducting experiments using various color schemes. In this repository, we make some folders to put the pictures based on color labels defined in the dataset in folder "Color_Classifiers-Primary_Color-CF1". The pictures from the dataset can be put in the folder "multiclass-DL classifier-primary-Training-(green/purple/red/yellow)". Which pictures are green or purple or red or yellow, can refer to "Training_Data_for_Color_of_Flower.txt". For Binary claasifier, put the dataset in the folder "binary-primary-Training-(Green/Non-Green)". All the pictures which have 'Green' labels, put in the folder "Green" and all the pictures except Green (Purple, Red, Yellow), put in the folder "Non-Green". Do the same action for Validation and Testing folders.
	
For Color of Flower (CF) in Primary Secondary Color using Color Scheme 2 and Color of Labellum (CL) in all scenarios, basically the codes are the same, only need to change the dataset for those scenarios.
