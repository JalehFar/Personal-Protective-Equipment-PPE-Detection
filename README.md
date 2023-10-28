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

1. `data` folder consists of the yaml file required for training. It also contains 3 folders train, valid and test. Each of these folders have 2 subfolders images (with .jpg files) and labels (with .txt annotations).
2. `results` folder consists of the prediction results of the model, confusion matrix plot, visualizations of the train and valid batches and PR curves.
3. `models` folder consists of 2 models, yolov8n.pt which is the pre-trained model on COCO128.yaml and best.pt which is the custom trained yolov8n model on our dataset.
4. `code` folder consists of videos and images for evaluation of our custom trained model.
5. `output` folder consists of output produced by our custom object detection model after 100 epochs of training.

## Code

```
├───.ipynb_checkpoints
├───assets
├───data
├───├──data.yaml
├───├──ppe_data.yaml
│   ├───test
│   │   ├───images
│   │   └───labels
│   ├───train
│   │   ├───images
│   │   └───labels
│   └───valid
│       ├───images
│       └───labels
├───models
├───output
│   └───output_yolov8n_100e
├───results
└───source_files
```

## Results

In order to have a fair comparison between the two models, we tried to choose the hyperparameters and the optimizer identical. Some of them are listed here.
- Epochs : 20
- Batch size : 16
- Optimizer : SGD
- Learning rate : 0.01
- Momentum : 0.937
- Execution Time: 
       - YOLOv8s completed 20 epochs in approximately 30 minutes.
       - YOLOv5s completed 20 epochs in approximately 41 minutes.
  ### Mean Average Precision(mAP)
  <img width="398" alt="image" src="https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/e699f752-a2e8-4acc-ad74-babf313c4288">
  <img width="414" alt="image" src="https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/083e6220-b960-411d-8ce4-8eefce274c0c">

  ### Confusion matrix:
  - YOLOv5s: ![confusion_matrix](https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/e7962d4b-09ee-44e9-bdd5-99b27e199aec)

  - YOLOv8s:  ![confusion_matrix_normalized](https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/b2aedd60-0c73-4689-9315-b31fb7fe8992)


![val_batch2_pred](https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/19fee64e-b9a1-412f-9a8d-e19c031fef5d)

## Results



https://github.com/JalehFar/Personal-Protective-Equipment-PPE-Detection/assets/117992631/df25cadc-1989-48fd-a0b8-bdf1e4cac79f





















