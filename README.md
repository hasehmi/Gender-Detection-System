# Real-Time Gender Detection System Using Machine Learning

## Project Description
This project develops a real-time gender classification system using computer vision and machine learning[cite: 2]. The system detects faces from a live webcam stream using OpenCV and classifies them as 'Male' or 'Female' using a `RandomForestClassifier`[cite: 2]. I built this project in a Google Colab environment, integrating JavaScript and Python to enable live video processing directly in the browser[cite: 2].

## Key Features & Achievements
* Trained a scikit-learn Random Forest Classifier using the `genderdetectionface` dataset from Kaggle, achieving an 86.76% accuracy[cite: 2].
* Implemented an image preprocessing pipeline using OpenCV (`cv2`) for grayscale conversion, resizing to 64x64, and flattening[cite: 2].
* Integrated Haar Cascade (`haarcascade_frontalface_default.xml`) for real-time facial detection from live video feeds[cite: 2].
* Accessed the browser's webcam by writing JavaScript code in Google Colab and processed live frames through a Python backend using base64 encoding and decoding[cite: 2].
* Created dynamic visual feedback to draw bounding boxes and display the model's prediction confidence percentages on live video frames[cite: 2].
