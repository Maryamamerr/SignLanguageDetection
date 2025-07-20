# SignLanguageDetection
🧠 Sign Language Recognition using LSTM and MediaPipe
This project is a real-time sign language recognition system using MediaPipe, OpenCV, and LSTM neural networks. It can detect and classify hand gestures like "hello", "thanks", and "I love you" using a webcam, and outputs the prediction using on-screen display and text-to-speech.
# 📁 Project Structure
 ```
├── main.py               # Run this to start real-time sign detection
├── preproccessing.py     # Data collection and preprocessing
├── training.py           # Train LSTM model on extracted keypoints
├── action.h5             # Saved trained model (generated after training)
├── MP_Data/              # Folder where keypoint data is saved
└── README.md             # Project documentation
 ```
# 🔧 Dependencies
Install required packages:
 ```
pip install opencv-python mediapipe tensorflow scikit-learn pyttsx3
 ```
# 🧩 How It Works
1. Data Collection (preproccessing.py)
Captures MediaPipe keypoints (face, pose, hands) from webcam.
Saves them as .npy files for each gesture (hello, thanks, i love you).

Run:
```
python preproccessing.py
```
3. Model Training (training.py)
Loads saved keypoints
Trains a 3-layer LSTM model
Saves the model as action.h5

Run:
```
python training.py
```
3. Real-time Prediction (main.py)
Loads the trained model
Captures webcam input
Predicts the performed gesture
Displays probabilities on screen
Speaks the prediction using pyttsx3

Run:
```
python main.py
```

📊 Model Performance
* Accuracy is printed after training
* Confusion matrix helps visualize prediction quality
  
✨ Features
* Real-time hand gesture detection
* Works offline (no internet required)
* Text-to-speech output
* Modular code for easy expansion

  🤝 Credits
* Developed using:

* MediaPipe

* TensorFlow

* OpenCV
