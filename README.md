# COVID-19_Chest_X-ray_Image_Generation_using_ResNet50_and_DCGAN_Model


This repository provides codes with datasets for the generation of synthesis images of Covid-19 Chest X-ray using DCGAN as generator and ResNet50 as discriminator from a set of raw covid-19 chest x-ray images, which are enhanced and segmented before passing through the DCGAN model.

# **Regarding contents of folders:**

The folder named ***1. Image Enhancement*** contains following contents 
1. code file (in .ipynb format) of covid-19 Chest X-ray image enhancement using Histogram Equalization techinque.
2. Sample of input of the above mentioned code (i.e. Covid-19 Chest X-ray raw grayscale images)
2. Sample of output of the above mentioned code (i.e. Covid-19 Chest X-ray enhanced images)


******
 The folder named ***2. Image Segmentation*** contains following contents 
1. code file (in .ipynb format) of covid-19 Chest X-ray segmentaed images using 3 different Segmentation techniques. These are:
    #### 1.  K-means Clustering
    #### 2. Mean Shift Clustering
    #### 3. Fuzzy C-means Clustering

2. Sample of output of each segmentation techniques.


******
The folder named ***3.Improvised DCGAN+ResNet50*** contains following contents 
1. code file (in .ipynb format) for generation of covid-19 Chest X-ray images. 
2. Models used:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. ResNet50 as Discriminator
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2. DCGAN as Generator 


******
# **Experimental Details:**

In this work, all the experiments are implemented in python 3.6.9 using two python frameworks, tensorflow $1.15.0$ and keras 2.3.1. For the visualization of the image samples python library matplotlib 3.4.3 is used. Moreover, numpy 1.15 is used to perform the intermediate operations in the code implementation. Furthermore, cv2, PIL, glob, sklearn python packages are also used in the code implementation. Finally, the whole process is executed in Dell precision $7820$ workstation configured with ubuntu $18.04$ $64$ bit Operating System, Intel Xeon Gold 5215 2.5GHz processor, 96GB RAM, and Nvidia 16GB Quadro RTX5000 graphics. 

## **Step-3: Image Enhancement**
* Image enhancement is performed to improve the quality and information content of original data before processing on Covid-19 Chest X-ray  raw grayscale images. Some sample images are shown below:
<img src="1.%20Image%20Enhancement/covid19_chest_Xray_raw_grayscale_images.jpg" width="480" >

* For that purpose, We have used the Histogram Equalization method. Some sample of Enhanced images are shown below:
<img src="1.%20Image%20Enhancement/Covid19_Chest_Xray_Enhanced_images.jpg" width="480" >

******
## **Step-2: Image Segmentation**
* The enhanced images are then segmented using three different clustering methods  to focus on the relevant parts of the images.. The methods are:
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1. K-means Clustering
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2. Mean Shift Clustering
#### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3. Fuzzy C-Means Clustering

* Some sample output of each Segmentation techniques are shown below:
<img src="2.%20Image%20Segmentation/Segmented_images.jpg" width="480" >

******
## **Step-3: Generation of Covid-19 Chest X-ray images using ResNet50+DCGAN**
* In our model, we have used ResNet50 as Discriminator and DCGAN as generator.
* Additionally, RAdam optimizer is used instead of Adam optimizer in DCGAN (Generator). 
* Trained the model with Segmented images of Covid-19 Chest X-ray using K-means clustering method as we achieved better accuracy with K-means Clustering method as compared to other merthods.
* Some sample of generated images are shown below:

<img src="3.%20Improvised%20DCGAN%2BResNet50/Generated%20images.jpeg" width="480" >

******
# **Datasets:**
Raw Covid-19 chest X-ray images are available in the given google drivelink provided below:

#### 1. Raw Covid-19 Chest X-ray Images 
  
    https://drive.google.com/drive/folders/1G_CwpObng9r2XVrLi5ou37IqFcZ6Bu42?usp=sharing
    
#### 2. Covid-19 Chest X-ray Enhanced Images
* Using Histogram Equalization
* Dataset Link:

      https://drive.google.com/drive/folders/106uANtZvTQzx7SdBIASJuqq3TBT8iWy3?usp=sharing
    
