# Pothole Detection using YOLOv8 Instance Segmentation

## Description
This project aims to detect and segment potholes using the YOLOv8 instance segmentation model. By leveraging deep learning techniques, it enables real-time pothole detection, which can aid in road maintenance and safety. The model is trained on annotated images and can be deployed for automated road inspections.

### Video Reference

Here is a sample video showcasing the model in action:

[![Pothole Detection Video](https://img.youtube.com/vi/4Evdb1je2M0/0.jpg)](https://www.youtube.com/watch?v=4Evdb1je2M0)


## Features
- Instance segmentation of potholes
- Trained using YOLOv8 with PyTorch
- Supports real-time inference
- Can be deployed on edge devices

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/narasimha07-here/pothole-detection.git
cd pothole-detection
pip install -r requirements.txt
```

## Dataset

The model is trained on a dataset containing annotated pothole images. Ensure your dataset follows the YOLO format:
- `images/train/`, `images/val/` directories for training and validation images.
- `labels/train/`, `labels/val/` directories for corresponding annotation files.

Modify `data.yaml` to specify dataset paths:

```yaml
path: /path/to/dataset
train: images/train
val: images/val
nc: 1
names: ['pothole']
```

## Training

Run the following command to train the model:

```bash
python train.py --model yolov8s-seg.pt --data data.yaml --epochs 50 --img 640
```

## Inference

Use the trained model to detect potholes in images or videos:

```bash
python detect.py --weights best.pt --source path/to/image_or_video
```

## Results

The model achieves accurate instance segmentation of potholes, making it suitable for road maintenance and safety applications.



## Future Improvements
- Experiment with different YOLOv8 versions
- Optimize for edge deployment
- Improve dataset annotations

## License
This project is open-source and available under the MIT License.

## Acknowledgments
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)

