```markdown
# Person Detection with Bounding Boxes

This repository provides a TensorFlow-based solution for detecting and bounding persons in images. It utilizes a pre-trained model from TensorFlow Hub for object detection and visualizes the results with bounding boxes and confidence scores.

## Features

- **Data Preprocessing:** Image augmentation for improved model training.
- **Model Integration:** Uses a pre-trained object detection model for bounding box detection.
- **Visualization:** Plots images with detected bounding boxes, center coordinates, and scores.

## Requirements

- TensorFlow
- TensorFlow Hub
- NumPy
- Matplotlib
- Python 3.x

## Setup

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Aryansansi/person-detection-bbox
   cd person-detection-bbox
   ```

2. **Install Dependencies:**

   ```bash
   pip install tensorflow tensorflow-hub numpy matplotlib
   ```

3. **Download the Dataset:**

   The dataset for training and testing the model can be downloaded from Kaggle:

   [Human Detection Dataset](https://www.kaggle.com/datasets/constantinwerner/human-detection-dataset)

   Download and extract the dataset into the `data_file` directory. Make sure the directory structure is as follows:

   ```
   data_file/
   ├── train/
   ├── validation/
   └── test/
   ```

4. **Download the Pre-trained Model:**

   The RCNN model can be obtained from Kaggle:

   [Faster RCNN Inception ResNet V2](https://www.kaggle.com/models/google/faster-rcnn-inception-resnet-v2/code)

   Follow the instructions on the Kaggle page to download the model and update the `model_url` in the code with the path to the downloaded model.

## Usage

1. **Run the Script for Person Detection and Bounding Boxes:**

   Execute the `main_rcnn.py` script to train and evaluate the model:

   ```bash
   python main_rcnn.py
   ```

2. **Scripts Available:**

   - **`detection.py`:** This script includes a model definition with convolutional layers, processes images in a grid format, and finds bounding boxes around detected persons. It evaluates the model and plots results with bounding boxes.
   - **`person_detection.py`:** This script uses the VGG16 model as the base, adds custom layers, and performs similar tasks as `detection.py` but with a VGG16-based model. It also processes images in a grid format, predicts bounding boxes, and plots results.

3. **Results:**

   The scripts will output images with detected bounding boxes and confidence scores.

## Acknowledgments

- The dataset is provided by [Constantin Werner](https://www.kaggle.com/datasets/constantinwerner/human-detection-dataset).
- The RCNN model is from [Google's Faster RCNN Inception ResNet V2](https://www.kaggle.com/models/google/faster-rcnn-inception-resnet-v2/code).

Feel free to contribute to this project by submitting issues and pull requests!
