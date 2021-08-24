An implementation of the paper - "Face Recognition System using Facenet Algorithm for Employee Presence" by Ferry Cahyono  et al. 2020

# Versions 
1) Python     - 3.8
2) Tensorflow - 2.5.0
3) Keras      - 2.4.3 

# Data Description
Color FERET - https://www.nist.gov/itl/products-and-services/color-feret-database - 111 subjects  
GeorgiaTech Face Database - http://www.anefian.com/research/face_reco.htm - 48 subjects  
KomNet Face Images Dataset - https://data.mendeley.com/datasets/hsv83m5zbb/2 - 50 subjects  

## Train/Test Split
### FERET
    Subjects - 111
    Total images - 1443 (13 per subject)
    Train images - 1110 (10 per subject)
    Test images - 333 (3 per subject)
### GeorgiaTech
    Subjects - 48
    Total images - 624 (13 per subject)
    Train images - 480 (10 per subject)
    Test images - 144 (3 per subject)
### KomNet
    Subjects - 50
    Total images - 650 (13 per subject)
    Train images - 500 (10 per subject)
    Test images - 150 (3 per subject)
  
For all the images in the created dataset, cropped face images were obtained and saved using the Multi-task Cascaded Convolutional Network (MTCNN) package in Keras.  
'sample_data' consists of the first ten subjects of the created dataset.

# Architecture
FaceNet was used to obtain feature vectors of the face images followed by Support Vector Machine (SVM) to classify the feature vectors by subjects.  
FaceNet weights can be obtain here: https://github.com/nyoki-mtl/keras-facenet

# Results
An **classification accuracy of 100%** was obtained on the dataset of 209 subjects.  
Given below is the visualization of the 2D feature vectors obtained by performing PCA analysis on the FaceNet outputs of 'sample_data' train images.

![Capture](https://user-images.githubusercontent.com/88875770/130456585-5d4aaa95-c42b-43a2-b84a-1f1a4cf56ce6.PNG)

# References
1. F. Cahyono, W. Wirawan and R. Fuad Rachmadi, "Face Recognition System using Facenet Algorithm for Employee Presence," 2020 4th International Conference on Vocational Education and Training (ICOVET), 2020, pp. 57-62, doi: 10.1109/ICOVET50258.2020.9229888.
2. https://github.com/nyoki-mtl/keras-facenet
3. Astawa, I Nyoman Gede Arya (2020), “KomNET: Face Image Dataset from Various Media”, Mendeley Data, V2, doi: 10.17632/hsv83m5zbb.2
