# Driver-Drowsiness-Detection-System
Driver Drowsiness Detection System This project implements a real-time driver drowsiness detection system using computer vision and facial landmark detection.
The system is designed to monitor a driver's eye and mouth movements to detect signs of drowsiness, such as prolonged eye closure and yawning. If drowsiness is detected, an alarm is triggered to alert the driver.

Features:
Eye Aspect Ratio (EAR) Calculation: Monitors the driver's eye closure by calculating the EAR. If the eyes remain closed for a predefined number of consecutive frames, a drowsiness alert is triggered.
Mouth Aspect Ratio (MAR) Calculation: Tracks the driver's mouth movements to detect yawning. The system keeps a count of yawns and displays it in real-time.
Real-Time Monitoring: Uses OpenCV to capture live video from the webcam and performs drowsiness detection on the video feed.
Alarm System: Plays a sound alert when the driver is detected to be drowsy.


Libraries and Tools:
OpenCV: For real-time video capture and image processing.
dlib: For detecting facial landmarks.
imutils: Utility functions for image processing.
playsound: To play sound alerts when drowsiness is detected.

How It Works:
The system captures video from the webcam and converts each frame to grayscale for processing.
It detects the face in the frame and identifies facial landmarks using dlib's pre-trained shape predictor.
The Eye Aspect Ratio (EAR) is calculated for both eyes, and the Mouth Aspect Ratio (MAR) is calculated for the mouth.
If the EAR falls below a certain threshold and remains there for a specified number of frames, a drowsiness alert is triggered.
If the MAR exceeds the yawning threshold, the system increments the yawn count.
The system displays the status of the eyes (open/closed), the current EAR and MAR values, and the yawn count on the video feed.
If drowsiness is detected, the system plays an alarm sound to alert the driver.
Prerequisites:
Python 3.x
OpenCV
dlib
imutils
playsound
shape_predictor_68_face_landmarks.dat (Dlib's pre-trained model for facial landmarks)


Usage:
Clone the repository and navigate to the project directory.
Ensure all dependencies are installed.
Run the script, and the system will start monitoring the driver's drowsiness in real-time.
Notes:
Make sure to place the shape_predictor_68_face_landmarks.dat file in the project directory.
Adjust the thresholds and frame count in the script as needed to fine-tune the detection accuracy.
