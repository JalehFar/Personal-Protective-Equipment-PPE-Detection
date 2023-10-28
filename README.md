# Personal-Protective-Equipment-PPE-Detection using YOLOv5 and YOLOv8

![c072f67c1f165bdd817516ef05837ef61c1dce3f](https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/1017e5fb-8d98-4328-9396-56ce0e2c7217)


## Introduction


Health and safety is a requirement in many industrial workspaces. Many incidents occur because workers do not use personal protective equipment (PPE) properly. To assure that all the workers follow these rules many companies and industries have tried using automated monitoring system to improve supervision. Automated monitoring device ensures the detection of full personal protective equipment and have a long lifetime and do not suffer from the errors by human monitoring. In this project the dataset provided by Roboflow on [PPE Object Detection](https://universe.roboflow.com/ardi-csjyk/ppe-hfjoc/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true) has been used. 
The dataset consists of 2497 image samples. These images are split into train: 2178(87%), valid: 199(8%) and test: 120(5%) sets. 

Overall, there are  7 classes in the dataset:

<img width="481" alt="image" src="https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/db37e89f-4442-4b8e-b697-6937452da933">

![image](https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/7f1973c0-c8ae-4084-aeb8-dc1e5e3a9165)

By adding some features to the code we were able to enhance the overall user experience and offer flexibility to adapt the PPE detection system to different environments. So, the users can choose the specific PPE equipment they want the model to detect.<img width="408" alt="image" src="https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/ad254dba-38b1-46c0-9dff-99479aa912c6">

## Setup

We installed the ultralytics library run YOLOv5 and YOLOv8 custom object detection on the dataset.

For more information check out these repositories: [Ultralytics YOLOv5](https://github.com/ultralytics/yolov5) and [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)


Note: These repositories contain all the results, visualizations and best model after custom training on the dataset.

## File Hierarchy

1.**data** folder consists of the yaml file required for training. It also contains 3 folders train, valid and test. Each of these folders have 2 subfolders images (with .jpg files) and labels (with .txt annotations).
2.results folder consists of the prediction results of the model, confusion matrix plot, visualizations of the train and valid batches and PR curves.
3.models folder consists of 2 models, yolov8n.pt which is the pre-trained model on COCO128.yaml and best.pt which is the custom trained yolov8n model on our dataset.
4.code folder consists of videos and images for evaluation of our custom trained model.
5.output folder consists of output produced by our custom object detection model after 100 epochs of training.









