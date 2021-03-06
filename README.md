# Embedded-CNN-based-vehicle-classification-and-counting-in-non-laned-road-traffic

## Prerequisites

Fork and Clone AlexeyAB's darknet folder on local host - https://github.com/AlexeyAB/darknet/tree/47c7af1cea5bbdedf1184963355e6418cb8b1b4f#how-to-train-to-detect-your-custom-objects

## Description
* YOLO(You Only Look Once) version 2 pretrained on Imagenet has been used as the base for the network. The network helps in object detection and classification by scanning test image only once. 

* To improve accuracy, we further trained this model on PASCAL VOC 2007 and KITTI Vision Benchmark Suite datasets. 

* The model thus obtained was fine-tuned on the various datasets listed below individually as well as cumulatively. The accuracy is has been mentioned for the respective test sets.

## Models

* For each model( except YOLO 5), the weights gathered in the 10,600th epoch was used to calculate the result. 

* For YOLO 5, we used the 72000th iteration weights. These specific models showed the best accuracy on the test data.

| Model        |Dataset           | Total Number of Annotated Images  | Accuracy(%) |Weights link  |
| ------------- |:-------------:| -----:| -----:| -----:|
| YOLO1      | Front View Fish Eye Lens Road Scene | 620 | 70.44 | https://drive.google.com/file/d/1sAiVgXM9dtv9rPsLd_ePQ66eTKce9HQD/view?usp=sharing |
|YOLO2     | Back View Under Flyover Road Scene     |   1189|  58.01|  https://drive.google.com/open?id=1QG5Ek03_E953lU97TkjVyE8su4fShA5j  |
| YOLO3 | DIMTS Heavy Vehicles Highway Scene   |  2754 |   62.32 |  https://drive.google.com/open?id=1GWlkHo0hL9cvR4b_GsynDJhiiAiGIT3G  |
| YOLO4 |Vehant Bus Low Light Road Scene |    999 |    34.86 | https://drive.google.com/open?id=1RzTYLlKZhiHuvIVWl2b4oqRL0owuGHd4   |
| YOLO5 | ALL of the above    |    5562 |    63.37 |  https://drive.google.com/file/d/1RzTYLlKZhiHuvIVWl2b4oqRL0owuGHd4/view?usp=sharing |

<img src="https://github.com/mansikhemka/Embedded-CNN-based-vehicle-classification-and-counting-in-non-laned-road-traffic/blob/master/t10.png" width="300" height="300">

<img src="https://github.com/mansikhemka/Embedded-CNN-based-vehicle-classification-and-counting-in-non-laned-road-traffic/blob/master/t11.png" width="300" height="300">

<img src="https://github.com/mansikhemka/Embedded-CNN-based-vehicle-classification-and-counting-in-non-laned-road-traffic/blob/master/t12.png" width="300" height="300">

<img src="https://github.com/mansikhemka/Embedded-CNN-based-vehicle-classification-and-counting-in-non-laned-road-traffic/blob/master/t7.png" width="300" height="300">


## Results

* For YOLO 5, 72000th iteration, following are the results:
  * For thresh = 0.25, TP = 4514, FP = 6036, FN = 1888, average IOU = 32.66%
  * For thresh = 0.25, precision = 0.43, recall = 0.71, F1-score = 0.53
  
## Dataset

If you are a researcher or student in an academic institution, please request our annotated dataset using your institutional email id from riju@cse.iitd.ac.in
