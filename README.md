# Fashion-Trend-Analysis

## TDP Vista Porject

This project is a Fashion Recommender System that uses a ResNet-50 neural network to extract image features and recommends similar fashion items based on an uploaded image.

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [How to Run](#how-to-run)

## Description

The Fashion Recommender System is built using Python and several libraries, including TensorFlow, Streamlit, and OpenCV. It allows users to upload an image of a fashion item, and the system recommends visually similar items from a pre-defined dataset based on feature extraction.

## Features

- Upload an image of a fashion item.
- Extract features from the uploaded image using a pre-trained ResNet-50 model.
- Use Nearest Neighbors to find the most visually similar fashion items.
- Display the top recommended fashion items.

## Prerequisites

Before running this project, ensure you have the following prerequisites:

- Python 3.7 or later
- TensorFlow
- Streamlit
- OpenCV
- Pillow
- NumPy
- tqdm
- sklearn

## Installation

1. Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/your-repo.git
cd your-repo
```

2. Install the required Python libraries using pip:

```bash
pip install tensorflow streamlit opencv-python-headless pillow numpy tqdm scikit-learn
```

3. Download the pre-trained ResNet-50 weights. You can do this using TensorFlow's Keras API or download the weights from the TensorFlow model zoo.

4. Organize your fashion item dataset in the following structure:

```
project-root/
  ├── images/
  │   ├── item1.jpg
  │   ├── item2.jpg
  │   ├── ...
  │
  ├── uploads/
```

## Usage

1. Run the feature extraction script to preprocess and save the image features:

```bash
python app.py
```

This script will save two pickle files, `embeddings.pkl` and `filenames.pkl`, containing the features and corresponding file paths.

2. Launch the Streamlit app:

```bash
streamlit run main.py
```

3. Access the app in your web browser. Upload an image of a fashion item to receive recommendations.

4. Additionally, you can test the recommendation system using a sample image by running the `test.py` script:

```bash
python test.py
```

## Code Structure

- `app.py`: Feature extraction script that pre-processes images and saves feature embeddings.
- `main.py`: Streamlit app for uploading images and displaying recommendations.
- `test.py`: A test script to check recommendations for a sample image.
