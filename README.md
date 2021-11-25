# NYCU_VRDL_Object_Detection
This is homework 2 in NYCU Selected Topics in Visual Recognition Deep Learning class.

NOTIFICATION:
Because the main code are too big, follow the link below to download it.
https://drive.google.com/file/d/120wryn8IRAiVxciyYO6KGjOj7Es5HzOa/view?usp=sharing

model weights link:
https://drive.google.com/file/d/19BDS4q4flsyEAiyRenIpNlEqeUWAVTgz/view?usp=sharing

# Hardware
The following specs were used to create the original solution.
* Google Colab
* PC
  * Intel(R) Core(TM) i7-7700 CPU @ 3.60GHz
  * NVIDIA RTX 1080 Ti

# Environment
```
cd yolov5
pip install mmcv
pip install -U pycocotools
pip install -r requirements.txt
```

# Dataset Preparation
Download this folder including dataset and put it in the same directory with yolov5 folder.
https://drive.google.com/file/d/1NEXWWJoLRW9R4RpK9EYYvPfvFFDPRTEE/view?usp=sharing

# Requirement
* Download and unzip 'datasets_final.zip'.
* There will include './my_datasets/images' and './my_datasets/labels' 
* Download and unzip the main code: https://drive.google.com/file/d/120wryn8IRAiVxciyYO6KGjOj7Es5HzOa/view?usp=sharing

# Train and Valid
You can customize your own batch size and epochs.
```
python train.py --img 640 --batch {} --epochs {} --data yrdl.yaml --weights yolov5l.pt
```
# Inference
The code not only trains, but also valid and test the model. You can run the model by following:
```
python detect.py --weights {} --conf 0.1 --source {}
```
Replacing the weights for './runs/train/exp/weights/best.pt' and source for your test data directory.

# References
YOLOv5:
https://github.com/ultralytics/yolov5
