# Flower Color Detection with a Fast Api Implementation

This repo is an implementation of some methods described in the paper "Automated color detection in orchids using color labels and deep learning". The method was proposed to detect Color of Flower (CF) and Color of Labellum (CL) in Orchids flower.

To use our code (redo our experiments):
1. Please setup the environment based on requirements.txt in the colab file.
2. The images for training, validation and testing should be put in different folders. 
3. The dataset (all of the images and the labels for training, validation and testing) can be downloaded from https://doi.org/10.7910/DVN/0HNECY. 
4. For using the images used in the method, please find the folder Color_Classifier. There are 2 folders: Multiple_Color and Primary_Color. Please use CF1, CF2, CL1 and CL2 folders for conducting experiments using various color schemes.
	
For Color of Flower (CF) in Primary Secondary Color using Color Scheme 2 and Color of Labellum (CL) in all scenarios, basically the codes are the same, only need to change the dataset for those scenarios. 

The Multi-Class Classifier was employed here using VGG16 with freezing only the first layer.

It was then deployed with fast api to be used to infer the colors of orchid flowers not seen before. 

Here is the link to the medium article detailing steps and procedures employed:
https://medium.com/@kwabenanyinaku/colour-detection-in-flowers-using-deep-learning-deployment-with-fastapi-84c28f0f84b9




# Refrences

https://github.com/d-harnoni 

https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0259036 

https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/0HNECY
