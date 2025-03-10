# YOLOv11_on_Rasp_Pi_4B
Run YOLOv11 for Real-Time Recognition on a Raspberry Pi model 4 B.

* Very useful sites to make YOLOv11 run:

<https://qengineering.eu/install-pytorch-on-raspberry-pi-4.html>

<https://github.com/Qengineering/RPi-Bullseye-DNN-image>

## 

# Setup Environment
* Raspberry Pi 4B (2 GB RAM + 2 GB swap)
* Operating System: Raspbian GNU/Linux 11 (bullseye)
* Distribution: raspberrypi 6.1.21-v8+
* OS type: 64-bit
* Software: Python 3.9.2 (same in the workspace)
* Environment: yoloenv (v-env)
* Object detection model: YOLO11n
* Segmentation model: YOLO11n-seg
* Pose detection model: YOLO11n-pose

See **_commands.txt_** and **_pip_freeze.txt_** for more details if interested.

## Failed attempts to make additional optimizations in order to run YOLOv11 faster on my Raspberry Pi 4
Several examples where I failed with an error message "Illegal instruction" although I managed to resolve the complicated dependencies between the installed packages:

#### Export a YOLO11n PyTorch model to ONNX format:
yolo export model=yolo11n.pt format=onnx  # export official model

#### Export a YOLO11n PyTorch model to ONNX format:
yolo export model=yolo11n.pt format=onnx dynamic=True

#### Export a YOLO11n PyTorch model to TensorFL format:
yolo export model=yolo11n.pt format=tflite int8=True   # export TensorFL model with INT8 quantization

## Note

The branches will be left unmerged to the master so that the files from Objects Detection, Segmentation and Pose Detection could be easily distinguished.

Only YOLOv8 on a laptop and YOLOv11 on a Raspberry Pi 4B (2 GB RAM) for the moment.

Next will be on a Nvidia Jetson Nano (4 GB RAM).
