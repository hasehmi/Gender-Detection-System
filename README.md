# Real-Time Gender Detection System Using Machine Learning

## Project Description
Is project mein computer vision aur machine learning ko istemal karte hue ek real-time gender classification system develop kiya gaya hai. Yeh system OpenCV ki madad se live webcam stream se faces detect karta hai aur `RandomForestClassifier` ka istemal karte hue unhe 'Male' ya 'Female' mein accurately classify karta hai. Is project ko Google Colab environment mein JavaScript aur Python ke integration ke sath banaya gaya hai takay browser mein hi live video processing ki ja sake.

## Key Features & Achievements
* **Machine Learning Model Training:** Kaggle ke `genderdetectionface` dataset ko istemal karte hue scikit-learn ka Random Forest Classifier train kiya jisne 86.76% accuracy achieve ki.
* **Computer Vision Pipeline:** OpenCV (`cv2`) ko use karte hue image preprocessing (grayscale conversion, resizing to 64x64, aur flattening) implement ki.
* **Real-Time Face Detection:** Haar Cascade (`haarcascade_frontalface_default.xml`) ko integrate kiya takay live video feed mein faces detect kiye ja sakein.
* **Colab & JavaScript Bridging:** Google Colab mein JavaScript code likh kar browser ke webcam ka access liya aur Python backend ke sath base64 encoding/decoding ke zariye live frames ko process karwaya.
* **Dynamic Visual Feedback:** Video frames ke upar real-time mein bounding boxes draw kiye aur model ki prediction confidence display karwai (e.g., "Male: 86.7%").
