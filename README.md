# Security Camera with Motion Detection

This project is a simple security camera system that detects motion using Python and OpenCV. The system captures video from the webcam and identifies significant movement in the frame. It highlights moving objects with bounding boxes and triggers a beep sound as an alert.

## Table of Contents
- [Features](#features)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Features
- **Motion Detection**: Continuously monitors webcam input to detect movement.
- **Bounding Box**: Draws a green rectangle around detected moving objects.
- **Audible Alert**: Plays a beep sound to notify the user of motion detection.
- **Thresholding and Contour Detection**: Converts frames to grayscale, applies Gaussian blur, and uses contour detection to identify regions with motion.

## How It Works
1. The webcam captures two consecutive frames.
2. The difference between the two frames is calculated to identify movement.
3. The difference image is converted to grayscale and blurred for smoother detection.
4. A binary threshold is applied to highlight areas of significant motion.
5. Contours are detected to outline the moving objects.
6. If a movement is detected above a certain size, a bounding box is drawn around the object and a beep sound is triggered.
7. The program runs in real-time, continuously analyzing new frames, and can be exited by pressing the 'q' key.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    ```

2. Navigate to the project directory:
    ```bash
    cd your-repo-name
    ```

3. Install the required dependencies using `pip`:
    ```bash
    pip install opencv-python
    ```

## Usage
1. Run the Python script:
    ```bash
    python security_camera.py
    ```
2. The webcam feed will open, and the program will start detecting motion. If significant movement is detected, a green bounding box will be drawn around the object, and a beep sound will play.

3. To exit the program, press the 'q' key.

## Dependencies
- Python 3.x
- OpenCV (`opencv-python`)
- winsound (for Windows beep alerts, pre-installed with Python on Windows)

## Contributing
Contributions are welcome! If you'd like to improve the project, please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
