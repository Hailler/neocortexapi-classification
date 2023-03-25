# Project:	Analyse Image Classification on Simple Shapes

## Project Description

The Image classification project is previously implemented using HTM algorithm and using NeoCortex API, where our primary task to experiment with simple shapes(circle, rectangle, square, triangle and star) on the spatial pooler parameters: Global/Local Inhibition, Potential Radius, Local Area Density and NumofActiveColumnsPerInArea and demonstrate how these parameters influence learning and generate a Best fit correlation matrix.

Further, The training data needs to be used for feature prediction of any given input image For example, the user after learning enter the image “Circle”. The prediction code provide a set of predicting results like: “Circle – 73%, Rectangle 14%, Triangle - 11%”.

 ## Setup for Learning and Prediction
 
 ### Step-1: Prepare the program's directory for learning Shapes
 
 Create a new folder "InputFolder/" in the project directory and the imagesets which are used to train the model are stored in it.
 
xxxxxx

 Each Imageset is stored inside a folder whose name is the set's label.
 
xxxxxx


### Step-2: Prepare the program's directory for Prediction Images.
 
 Create a new folder "PredictInputFolder/" in the project directory and the Prediction Images are stored in it, where the prediction extracts the images from this directory to perform the shape prediction with the help of trained dataset. The prediction code is able to get the multiple images for prediction and displays the similarity output respectivly

 xxxxxxx


## Tasks and Results

### Task 1: To change the various learning parameters and find the best fit that shows image classification. 

The following parameters have been changed for the trained image dataset of simple shapes. 

| Parameter       | Description         |
| ------------- |:-------------:|
| POTENTIAL_RADIUS      |Defines the radius in number of input cells visible to column cells. It is important to choose this value, so every input neuron is connected to at least a single column. |
| GLOBAL_INHIBITION      |If TRUE global inhibition algorithm will be used. If FALSE local inhibition algorithm will be used. |
| LOCAL_AREA_DENSITY      |Density of active columns inside of local inhibition radius. If set on value < 0, explicit number of active columns (NUM_ACTIVE_COLUMNS_PER_INH_AREA) will be used. |
| NUM_ACTIVE_COLUMNS_PER_INH_AREA     |An alternate way to control the density of the active columns. If this value is specified then LOCAL_AREA_DENSITY must be less than 0, and vice versa. |

After experimenting the learning dataset with the various parameters, we were able to find the best corelation matrix that shows image classification for simple shapes.

xxxxx

### Task 2: Code for Image Prediction. 

1. After the learning process, The prediction images are extracted from the "PredictInputFolder/".(Multiple images can be provided as input for the prediction where the code is able to loop between them and display the similarity results respectively)
2. The images are encoded and input pattern is learned.
3. The Prediction method compares the predict image SDR with the trained image SDR's and caluclates the average percentage of similarity for a shape.
4. The Prediction code will display the average percentage between the input predict image and trained shapes.

The flowchart of the prediction phase is demonstrated in the below image

xxxxxxxxx

Below is the prediction result for the images used for predicion
xxxxxxx


## Goals Accomplished

Learning Phase:
1. Conducted several experiments with two different datasets having image dimensions 100x100 and 64x64 for influencial learning.
2. Experimented the spatial pooler parameters with different values of PotentialRadius, LocalAreaDensity, NumActiveColumnsPerInhArea and Global Inhibition and plotted graphs for the detailed understanding between them. 
3. Generated the execution times graph for the different PotentialRadius and LocalAreaDensity values.
4. Able to find the best fit matrix for both the datasets.

Prediction Phase
1. Implemented the prediction code and tested the accuracy with three different images
