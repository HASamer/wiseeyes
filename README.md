# wiseeyes
# WiseEyes: Drowsiness and Eye Blink Detection, and Object Detection

## Overview
WiseEyes is a comprehensive project that combines two critical functionalities: Drowsiness Detection and Eye Blink Detection. These features significantly contribute to safety and attentiveness using advanced computer vision techniques.

## Drowsiness Detection with YOLO
This component employs the YOLO (You Only Look Once) object detection model to identify signs of drowsiness in individuals. The project determines whether a person is awake or drowsy based on visual cues.

### Requirements
- Python 3.x
- Pip package manager
- Ultralytics library
- Pre-trained YOLO model weights file (e.g., 'best.pt')
- Training data in YAML format (e.g., 'data2.yaml')

### Installation
```bash
pip install ultralytics
```

### Training
Prepare training data in YAML format and load a pre-trained YOLO model:
```python
model = YOLO('yolov8n.yaml') # load pretrained model
```

### Prediction
Replace paths accordingly and perform predictions:
```python
model = YOLO("/path/to/best.pt")
```

### Results
Prediction results will be printed, and visual output (if show=True) will display predicted bounding boxes. Customize code and parameters for your specific use case and dataset.

## Eye Blink Detection and Position Estimation
This Python script utilizes the Mediapipe library for eye blink detection and eye position estimation.

### Requirements
Ensure the necessary libraries are installed:
```bash
pip install opencv-python mediapipe numpy
```

### Usage
Run the script with the following command:
```bash
python your_script_name.py
```
Press 'Q' to exit the video stream.

### Features
- Eye blink detection using facial landmarks.
- Estimation of eye position (right, center, left) based on pixel analysis.
- Real-time display of frames per second (FPS) and total blink count.

### Landmark Indices, Constants, and Variables
The script utilizes specific indices for facial landmarks, constants for blink detection, and variables to track blink counts.

## Credits
This script was developed by IEEE ENICarthage SB as part of WiseEyes. Contributions and feedback are welcome. Feel free to contribute and provide feedback to enhance the capabilities of WiseEyes.

## Object Detection in Driving Scenarios
To detect objects when driving with a camera in the car, use the following command:
```bash
!python examples/val.py --tracking-method deepocsort --benchmark MOT17-mini --imgsz 320 --conf 0.2
```

## Integration with WiseEyes
This code snippet can be integrated with WiseEyes for enhanced safety and attentiveness. Please refer to the WiseEyes documentation for further instructions.

## Credits
This code was developed as part of the WiseEyes project. Contributions and feedback are welcome.
