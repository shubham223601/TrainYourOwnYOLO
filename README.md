# Train custom data YOLO model: 

## Annotate the images
use Microsofts https://github.com/Microsoft/VoTT/releases for anotating
1. create a new project and call it Annotations
2. choose TrainYourOwnYOLO/Data/Source_Images/Training_Images as the Source and Target Connection
3. under export setting choose CSV as provider and save the changes
4. start labelling the region of interest
5. once labeled press CTRL+E to export the project
6. inside path TrainYourOwnYOLO/Data/Source_Images/Training_Images, you will find a csv folder called vott-csv-export containing Annotations-export.csv
7. in path TrainYourOwnYOLO/Image_Annotation run the script to convert the annotation to YOLO accepted format

## Training -  Download the pre-trained dark-net weights and convert them to YOLO format
1. from path TrainYourOwnYOLO/2_Training run python Download_and_Convert_YOLO_weights.py
2. train the model using python Train_YOLO.py

## Test on new Dataset
1. python Detector.py from path TrainYourOwnYOLO/3_Inference
