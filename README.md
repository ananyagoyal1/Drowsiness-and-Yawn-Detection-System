# Drowsiness and Yawn Detection System

This project implements a computer vision-based system to detect drowsiness and yawning in real-time video streams. It leverages facial landmark detection and eye aspect ratio calculations to monitor the user's eye movements and mouth openings. When drowsiness or yawning is detected, the system triggers an audible alarm to alert the user.

## Features

- **Drowsiness Detection**: The system continuously tracks the user's eye aspect ratio (EAR) using facial landmarks. If the EAR drops below a predefined threshold for a certain number of consecutive frames, it indicates that the user is drowsy, and an alarm is triggered.

- **Yawn Detection**: By monitoring the distance between the upper and lower lips, the system can detect when the user yawns. If the lip distance exceeds a specified threshold, an alarm is sounded to alert the user.

- **Real-time Video Processing**: The system processes live video streams from a webcam or other video sources, providing real-time detection and alerting capabilities.

- **Audible Alarm**: When drowsiness or yawning is detected, the system plays an audible alarm (WAV file) to alert the user and prevent potential accidents or mishaps.

## Prerequisites

Before running the Drowsiness and Yawn Detection System, ensure that you have the following dependencies installed:

- Python 3.x
- OpenCV (cv2)
- dlib
- imutils
- NumPy
- scipy
- playsound (optional, for audible alarms)

You can install the required Python packages using pip:

```
pip install opencv-python dlib imutils numpy scipy playsound
```

Additionally, you'll need to download the pre-trained facial landmark detector model from the dlib library and place it in the project directory. The model file is named `shape_predictor_68_face_landmarks.dat`.

## Usage

1. Clone the repository to your local machine:

```
git clone https://github.com/your-username/drowsiness-yawn-detection.git
```

2. Navigate to the project directory:

```
cd drowsiness-yawn-detection
```

3. Run the `drowsiness_yawn.py` script with the appropriate arguments:

```
python drowsiness_yawn.py --webcam <webcam_index> --alarm <alarm_file_path>
```

Replace `<webcam_index>` with the index of the webcam on your system (typically 0 for the default webcam), and `<alarm_file_path>` with the path to the audible alarm file (e.g., `Alert.WAV`).

4. The system will start processing the video stream from the specified webcam. If drowsiness or yawning is detected, an audible alarm will be played.

5. Press 'q' to exit the program.

## Customization

The Drowsiness and Yawn Detection System can be customized and extended to meet specific requirements. Here are a few potential modifications:

- **Adjust Thresholds**: Modify the `EYE_AR_THRESH` and `YAWN_THRESH` values to adjust the sensitivity of drowsiness and yawn detection, respectively.
- **Change Alarm Sound**: Replace the audible alarm file with a different sound file of your choice.
- **Integrate with Other Systems**: Integrate the detection system with other applications, such as vehicle safety systems or workplace monitoring systems.
- **Facial Landmark Model**: Use a different pre-trained facial landmark model or train a custom model for better performance on specific domains.
- **Logging and Reporting**: Implement logging and reporting mechanisms to track detection events and generate reports for analysis.

## Contributing

Contributions to the Drowsiness and Yawn Detection System are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request on the GitHub repository.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

- OpenCV for providing the computer vision library used in this project.
- dlib for the facial landmark detector and pre-trained model.
- imutils for image processing utilities.
- NumPy and SciPy for numerical computing support.
- playsound for playing audible alarms (if used).
