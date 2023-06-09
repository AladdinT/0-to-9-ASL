# 0 to 9 American Sign Language Model
<img src="https://raw.github.com/AladdinT/0-to-9-ASL/master/media/asl_numbers.png"  width="500">
<br>
Estimates hand pose using MediaPipe.<br> 
This is a sample program that recognizes hand gestures with a simple MLP using the detected key points.

<br> 

_️**This is forked from [kinivi/hand-gesture-recognition-mediapipe](https://github.com/kinivi/hand-gesture-recognition-mediapipe).**_
<br>


# Demo
Here's how to run the demo using your webcam.
```bash
python app.py
```
<br>
<img src="https://raw.github.com/AladdinT/0-to-9-ASL/master/media/animation.gif" width="200" height="150">

<br>

The following options can be specified when running the demo.
* --device<br>Specifying the camera device number (Default：0)
* --width<br>Width at the time of camera capture (Default：960)
* --height<br>Height at the time of camera capture (Default：540)
* --use_static_image_mode<br>Whether to use static_image_mode option for MediaPipe inference (Default：Unspecified)
* --min_detection_confidence<br>
Detection confidence threshold (Default：0.6)
* --min_tracking_confidence<br>
Tracking confidence threshold (Default：0.5)

# Directory
<pre>
│  app.py
│  keypoint_classification.ipynb
│  point_history_classification.ipynb
│  
├─model
│  └─keypoint_classifier
│     │  keypoint.csv
│     │  keypoint_classifier.hdf5
│     │  keypoint_classifier.py
│     │  keypoint_classifier.tflite
│     └─ keypoint_classifier_label.csv
│
└─utils
    └─cvfpscalc.py
</pre>
### app.py
This is a sample program for real-time inference.<br>
You can also collect training data (key points) for hand sign recognition.<br>


### model_training.ipynb
This is a model training script for hand sign recognition.<br>
please refer to [main repo](https://github.com/kinivi/hand-gesture-recognition-mediapipe) for better understanding of how the data collection and training process works. 

<br>

## Confusion Matrix 

![confusion matrix](https://raw.github.com/AladdinT//0-to-9-ASL/master/media/output.png)


### model/keypoint_classifier
This directory stores files related to hand sign recognition.<br>
The following files are stored.
* Training data(keypoint.csv)
* Trained model(keypoint_classifier.tflite)
* Label data(keypoint_classifier_label.csv)
* Inference module(keypoint_classifier.py)

### utils/cvfpscalc.py
This is a module for FPS measurement.
