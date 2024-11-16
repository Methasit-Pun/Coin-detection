# Coin Detection Program: Real-time Size Measurement & Separation

## Project Overview
This project involves the development of a coin detection system using a webcam to detect and measure the size of coins in real-time. The system is designed as a prototype for a future application in detecting and sorting nuts and bolts based on size. The program captures video from the webcam, processes the frames to detect the coins, measures their size, and categorizes them accordingly.

### Key Features:
- Real-time coin detection through webcam feed.
- Measurement of the coin's diameter.
- Separation of coins based on size (categorized into different classes).
- Designed as a prototype for nuts & bolt detection algorithm in Mechatronics.

### Purpose:
This program aims to demonstrate the capability of real-time image processing and size measurement in an automated detection system, which is later intended to be adapted for industrial applications such as nuts and bolt sorting in the manufacturing process.

---

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Algorithm Explanation](#algorithm-explanation)
4. [Dependencies](#dependencies)
5. [Project Structure](#project-structure)
6. [Future Enhancements](#future-enhancements)

---

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/coin-detection.git
   cd coin-detection
   ```

2. **Install Required Libraries:**

   This program uses Python and OpenCV for image processing and computer vision tasks. To install the necessary dependencies, run:

   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

1. Connect a webcam to your computer.
2. Run the `coin_detection.py` script to start the detection program.

   ```bash
   python coin_detection.py
   ```

3. The program will display the live feed from the webcam, process the frames, detect coins, measure their size, and categorize them based on predefined size ranges (small, medium, large).
4. The categorized coins will be printed in the terminal along with their sizes.

---

## Algorithm Explanation

The algorithm for detecting and measuring coins in real-time involves the following steps:

1. **Capture Video Feed**: Use OpenCV to access the webcam and continuously capture video frames.
2. **Pre-processing**: Convert the captured frames to grayscale and apply Gaussian Blur to reduce noise.
3. **Edge Detection**: Use Canny edge detection to find the edges of the coins in the image.
4. **Contour Detection**: Find contours of the detected edges, which helps in identifying the individual coins.
5. **Circle Detection**: Apply the Hough Circle Transform to detect circular shapes in the image, which corresponds to coins.
6. **Size Measurement**: Measure the diameter of each detected circle (coin) and classify it into categories (small, medium, large).
7. **Display Results**: The program will highlight the detected coins, display their size, and categorize them.

---

## Dependencies

The following Python libraries are required to run the program:

- **OpenCV**: For real-time computer vision and image processing.
- **NumPy**: For numerical operations and array handling.
- **Matplotlib** (optional): For visualizing processed images and results.

To install all dependencies, use the following:

```bash
pip install opencv-python numpy matplotlib
```

---

## Project Structure

```
coin-detection/
│
├── coin_detect_image.py        # coin detection from jpg file
├── cam.py                      # Camera calibration using coins
├── cam2.py                     # Captures real-time video from the webca and classifies coins based on their radius into predefined categories (5 baht, 10 baht, or unrecognized)
├── cam3_newalgo.py             # Detects circular coins using Hough Circle Transform, assigns unique colors to each coin size, and displays the detected coins with their radii and coordinates
├── requirements.txt            # List of required libraries for installation
├── README.md                   # Documentation for the project
└── images/                     # Folder for test images (optional)
```

---

## Future Enhancements

- **Nuts & Bolts Detection**: Adapt the coin detection system for industrial applications like nuts and bolts sorting based on size.
- **Machine Learning Integration**: Integrate machine learning models to improve detection accuracy, especially in cluttered or overlapping objects.
- **Real-time Sorting System**: Build an automated sorting mechanism that physically separates detected coins (or nuts and bolts) using motors and actuators controlled by the Raspberry Pi or microcontroller.
- **Multiple Object Detection**: Extend the system to detect and separate multiple types of objects, including washers, screws, and other components.

---

## Credits
This project was developed as a prototype for the Mechatronics 3rd-year semester 1 project at Chulalongkorn University.

---

Feel free to modify and expand this README based on the specific details of your project!
