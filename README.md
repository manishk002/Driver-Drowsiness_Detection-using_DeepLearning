# Driver Drowsiness Detection using Deep Learning

This project implements a real-time driver drowsiness detection system using deep learning techniques. It aims to enhance road safety by monitoring a driver's eye state and alerting them when signs of fatigue are detected.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)

## Overview

Driver fatigue is a significant cause of road accidents. This project uses computer vision and deep learning to detect driver drowsiness in real-time. By monitoring the driver's eyes, the system can alert the driver when they appear to be falling asleep, potentially preventing accidents.

## Features

- Real-time eye state detection (open/closed)
- Face and eye detection using Haar Cascades
- Deep learning model (InceptionV3) for eye state classification
- Audio alert system when drowsiness is detected
- Easy-to-use interface with live video feed and drowsiness score

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/manishk002/Driver-Drowsiness-Detection-using--DL.git
   cd Driver-Drowsiness-Detection-using--DL
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Download the pre-trained model file `model.h5` and place it in the `models` directory.

## Usage

Run the main script to start the drowsiness detection system:

```
python main.py
```

The system will access your computer's webcam and start monitoring. An alert will sound if the driver's eyes remain closed for too long.

## Project Structure

- `data_preparation.py`: Script for preparing and organizing the dataset
- `model_training.py`: Script for training the InceptionV3 model
- `main.py`: Main script for running the drowsiness detection system
- `models/`: Directory containing the trained model
- `MRL Eye Data/`: Dataset used for training (not included in the repository)

## Model Training

The model was trained on the MRL Eye Dataset. To retrain the model:

1. Prepare the dataset using `data_preparation.py`
2. Run the training script:
   ```
   python model_training.py
   ```

The script uses transfer learning with InceptionV3 as the base model and adds custom layers for eye state classification.

## Contributing

Contributions to improve the project are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Dataset link

http://mrl.cs.vsb.cz/eyedataset

## License

Distributed under the MIT License. See `LICENSE` file for more information.
