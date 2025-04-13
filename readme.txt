# AI Gym Movement Tracker

A computer vision-based workout tracking system that can detect, count, and provide feedback on various exercise movements using a webcam or video input.

## Features

- Real-time pose detection and tracking
- Automatic exercise classification (pushups, squats)
- Rep counting with form validation
- Visual feedback on exercise form
- Progress tracking with percentage bars

## Dependencies

- Python 3.6+
- OpenCV (`opencv-python`)
- TensorFlow 
- MediaPipe
- NumPy
- Matplotlib
- Argparse

## Installation

1. Clone the repository
2. Install the required dependencies:

```
pip install -r requirements.txt
```

## Usage

### Running with Webcam


python main.py --webcam


### Running with a Video File


python main.py --video resources/c.mp4


### Basic Pushup Counter

For a simpler pushup counter without exercise classification:

```
python push_up_counter_work.py
```

## Controls

- Press `q` or `Esc` key to exit the program at any time

## How It Works

1. The system uses MediaPipe to detect body pose landmarks
2. A trained classifier identifies the type of exercise being performed
3. Based on the exercise, specific angle calculations are used to track form
4. Repetitions are counted when proper form is maintained throughout a complete movement

## Supported Exercises

- Pushups
- Squats

## Project Structure

- `integration.py` - Main application with exercise classification
- `push_up_counter_work.py` - Simplified pushup counter
- `Classifier.py` - Exercise classification model
- `models/` - Contains trained model files
- `utils/` - Utility functions and helpers
- `resources/` - Additional resources and assets
