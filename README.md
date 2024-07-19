# Image-Segmentation of Handwritten Digit 
## Overview
This project focuses on the segmentation of handwritten digit images. The goal is to accurately identify and separate individual digits from a given image, which may contain multiple digits. This process is crucial for applications such as Optical Character Recognition (OCR) and automated data entry.

## Dataset
The dataset used for this project is a collection of handwritten digit images. Each image may contain one or more digits, and the task is to segment these digits accurately.

## Source
The dataset is sourced from:
 ### 1. MNIST Database
 ### 2. Custom images created and annotated for this project

## Installation
To set up the project, follow these steps:

1. Clone the repository:
```
git clone https://github.com/gaytri9/image_segmentation.git
```
2. Navigate to the project directory:
```
cd image_segmentation
```
3. Create a virtual environment:
```
python -m venv venv
```
4. Activate the virtual environment:
   
    4.1 On Windows:
   ```
   venv\Scripts\activate
   ```
   4.2 On macOS and Linux:
   ```
   source venv/bin/activate
   ```
 5. install the required packages:
```
pip install -r requirements.txt
```

## Usage
To run the segmentation model on the test images, follow these steps:

1. Ensure your dataset is in the data directory. The directory structure should look like this:

```
data/
    train/
        0/
        1/
        ...
        9/
    test/
        *.png
```
2. Preprocess the dataset:
```
python preprocess.py
```
3. Train the model:
```
python train.py
```
4. Segment digits in the test images:
```
python segment.py --input_dir data/test --output_dir output/segmented
``` 
## Directory Structure
```
handwritten-digit-segmentation/
│
├── data/
│   ├── train/
│   └── test/
│
├── output/
│   └── segmented/
│
├── src/
│   ├── preprocess.py
│   ├── train.py
│   └── segment.py
│
├── models/
│   └── digit_segmenter.h5
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Files
1. preprocess.py: Preprocesses the dataset for training.
2. train.py: Trains the segmentation model.
3. segment.py: Segments the digits in the test images.
4. digit_segmenter.h5: The trained model.
   
## Model Architecture
The model architecture is based on a Convolutional Neural Network (CNN) designed for image segmentation. It includes:
1. Convolutional layers for feature extraction
2. Max-pooling layers for down-sampling
3. Fully connected layers for classification

## Evaluation
The model's performance is evaluated using metrics such as:
1. Accuracy
2. Precision
3. Recall
4. F1 Score
Results are visualized using plots and confusion matrices.

## Contributing
Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (git checkout -b feature/your-feature).
3. Make your changes.
4. Commit your changes (git commit -m 'Add your feature').
5. Push to the branch (git push origin feature/your-feature).
6. Create a new Pull Request.
