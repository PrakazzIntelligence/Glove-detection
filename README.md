# Glove-detection
Detection of gloves in the hands of employees through the survillence cameras 

Video feed is taken from the survillance feed of the CCTV footages. 

Done through Custom weight file generation.

Annotations are taken from the footage frames and get stored. 

Annotation files provided in seperate class files contatining the seperate classes

Annotation folder contains .jpg and .txt with their respective annotations


Annotations/

|-Nglove  #containing annotations and corresponding images of persons not wearing gloves for training process

|-glove #containing annotations and corresponding images of persons wearing gloves for training process

Config folder contains the necessary files that are required for training the object

Config files/

|-obj.data #contains path directories of the data for feeding into the training process.

|-obj.names #class names of the objects

|-yolo-obj.cfg #contains the configurations of the yolo neural network structure\

|-train.txt #contains location of the images for feeding into the training

|-test.txt #contains location of the images for testing part1


Darknet folder containing the structure of the darknet which is going to be customized containing the weight and 

configuration files/ 

|-darknet/

For the training structure, darknet57.conv74 has been used and can be downloaded from the below link

wget https://pjreddie.com/media/files/darknet53.conv.74

**A video with person discovery is done with the pretrained weights is shown in pretrained_output.mp4

Training Process:
Input : Convert the video into frames and annotate the images 
Format: Annotations is taken in the yolo data format

Config files:

- Create a obj.names containing the names of the classes

- Create a obj.data file specifying the location of each specified files.

- Create a yolo-obj.cfg file containing the structure in specification with classes for Neural network layers

Now run the file (in Ubuntu) - ./darknet detector train <config file> <data file> <training network>
   compile
  
  After successful training a yolo-obj.weight file will be generated.

The glove detection process is on training. 
