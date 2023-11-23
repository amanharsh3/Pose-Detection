# Pose Estimation using Keras OpenPose

## Overview

This repository contains code for multi-person pose estimation using the Keras implementation of OpenPose. The model is based on the VGG architecture and is capable of detecting key body joints and their connections in an image.

### Prerequisites

- [Python 3](https://www.python.org/downloads/) 
- [Git](https://git-scm.com/)
- [TensorFlow](https://www.tensorflow.org/install)
- [Cython, scikit-image, pandas, zmq, h5py, opencv-python, configobj](requirements.txt)

### Installation

Clone the repository and set up the required model files:

```bash
git clone https://github.com/amanharsh3/Pose-Detection.git
```

## Usage

### Running Pose Estimation on an Image

1. **Load the Pretrained Model Weights:**

    ```python
    from tensorflow.keras.models import load_model

    weights_path = "model/keras/model.h5"
    model = load_model(weights_path)
    ```

2. **Apply the Model to an Image:**

    ```python
    # Load an image
    img = load_image("path/to/your/image.jpg")

    # Run pose estimation
    heatmaps, pafs = model.predict(img)
    ```

3. **Visualize the Results:**

    ```python
    # Visualize keypoints and PAFs
    visualize_results(img, heatmaps, pafs)
    ```

Adjust the file path in the `load_image` function to point to the image you want to perform pose estimation on.

**Note:** Ensure that you have the required Python packages and dependencies installed before running the code.
