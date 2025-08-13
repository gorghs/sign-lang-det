Live Sign Language Detector

A real-time sign language detection system that captures live video from a webcam, recognizes hand gestures, and translates them into sign language labels using a Convolutional Neural Network (CNN).

This tool is designed for accessibility, communication, and learning, allowing non-signers and sign language users to bridge the communication gap.


---

📌 Features

Real-Time Gesture Recognition – Detects signs instantly from your camera feed.

Multiple Modes – With GUI or without GUI (command line only).

Data Collection Support – Easily collect and label your own dataset for training.

Pre-Trained Model Included – No need to train from scratch to get started.



---

🛠️ Project Structure

File	Description

cnn8grps_rad1_model.h5	Pre-trained CNN model for gesture classification
data_collection_binary.py	Script to collect binary-labeled gesture data
data_collection_final.py	Script to collect the final multi-class dataset
final_pred.py	Live sign detection with GUI display
prediction_wo_gui.py	Live sign detection without GUI (console output)
white.jpg	Asset image used in GUI display



---

🚀 Installation

1️⃣ Clone the Repository

git clone https://github.com/gorghs/sign-lang-det.git
cd sign-lang-det

2️⃣ Install Dependencies

If requirements.txt exists:

pip install -r requirements.txt

If not, install manually:

pip install opencv-python tensorflow numpy


---

📖 Usage

📷 Data Collection

Binary Mode (one gesture vs. background):


python data_collection_binary.py

Multi-Class Mode (full gesture set):


python data_collection_final.py

🔍 Prediction

With GUI:


python final_pred.py

Without GUI:


python prediction_wo_gui.py


---

🧠 How It Works

1. Captures video from the webcam using OpenCV.


2. Preprocesses the frame (resize, grayscale, normalization).


3. Uses the CNN model (cnn8grps_rad1_model.h5) to classify the gesture.


4. Displays or prints the predicted sign in real-time.




---

📌 Model Details

Model Type: Convolutional Neural Network (CNN)

Input: Preprocessed hand gesture image

Output: Class label of detected gesture

Limitations:

Works best in good lighting

Camera should clearly capture the hand

Accuracy depends on training dataset




---

📜 License

This project is licensed under the MIT License – free to use and modify with attribution.


---

🤝 Contributing

Contributions are w
elcome!
Fork the repository, make your changes, and submit a pull request.
