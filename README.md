# Glove-detection
Detection of gloves in the hands of employees through the survillence cameras 

Video feed is taken from the survillance feed of the CCTV footages. 

Annotations are taken from the footage frames and get stored. 

Annotation files provided in seperate class files contatining the seperate classes

Annotation folder contains .jpg and .txt with their respective annotations


Annotations/
|-Nglove  
|-glove

Config folder contains the necessary files that are required for training the object

Config files/
|-obj.data #contains path directories of the data for feeding into the training process.
|-obj.names #class names of the objects
|-yolo-obj.cfg #contains the configurations of the yolo neural network structure
|-train.txt #contains the images for feeding into the training
|-test.txt #contains images for testing part1

Darknet folder containing the structure of the darknet which is going to be customized containing the weight and configuration files 
|-darknet/

For the training structure, darknet57.conv74 has been used. 
