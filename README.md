# Face-Recognition
A Web App integrated with ML models to recognize human faces

## Install
1. Install Anaconda Python
2. Install virtural environment
3. Activate virtual environment
   ```sh
   source freeai/bin/activate
   ```
4. Install dependencies in requirement.txt
   ```
   pip install -r requirements.txt
   ```
5. Install OpenCV

## Develop Face Recognition model
1. Data preprocessing including cropping face, adjust the size, EDA, normalization
2. Feature extraction using PCA to flatten to eigen faces
3. Utilize machine learning model SVM to classify and conduct model evaluation

## Integrate to Falsk App
1. Build base HTML
2. Frontend of face recognition and gender classification page
3. How to run the web app
   ```
   python main.py
   ```
