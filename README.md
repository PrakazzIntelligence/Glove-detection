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

Timelines and guidelines


**The model development is explained as follows. 
Intially, the footage from the CCTV is downloaded in the form of a video and converted into each frame per second for processing the frames with better clarity. 
The frames are then needed to be annotated for specifying the object to be identified.
The objects present in the frames are annotated and processed onto yolo format.
The yolo format data contains bounding values for the annotations.
The locations of the files are specified onto a training file and reduced into a testing file
A customized neural network in the form of darknet is taken.
The network structure is given the form of darknet53.conv74 file.
The configuration files are also created and the training process is initiated with darknet, obj.data and yolo-obj.cfg file(containing the custom neural network).
After, the training a weight file will be generated which can be deployed into the model.

Length of the video:  2mins 54 secs

S.No 	Tasks	Activities 	Time taken (in hrs)
1.	Frame conversion	Time spent for conversion of frames	0.04
2.	Glove Annotation	Time taken for annotation	0.30
3.	Creating Config files	Time taken for specifying config files	3.0
4.	Customizing neural networks	Time taken for customizing neural network structure	0.30
5.	Testing pretrained model	Time taken for testing the pretrained weight model	0.15
**Total time taken	4.19 hrs
