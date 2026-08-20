# Real Time Gender Detection System Using Machine Learning

## Project Description
This project develops a real time gender classification system using computer vision and machine learning. The system detects faces from a live webcam stream using OpenCV and classifies them as 'Male' or 'Female' using a RandomForestClassifier. I built this project in a Google Colab environment and integrated JavaScript and Python to enable live video processing directly in the browser.

## Key Features
* Trained a scikit learn Random Forest Classifier using the genderdetectionface dataset from Kaggle to achieve an 86.76% accuracy.
* Implemented an image preprocessing pipeline using OpenCV for grayscale conversion, resizing to 64x64, and flattening.
* Integrated Haar Cascade for real time facial detection from live video feeds.
* Accessed the browser webcam by writing JavaScript code in Google Colab and processed live frames through a Python backend using base64 encoding and decoding.
* Created visual feedback to draw bounding boxes and display the model prediction confidence percentages on live video frames.
