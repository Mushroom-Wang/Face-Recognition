# Welcome to Face Recognition Web App by Quan Wang
This is a web app integrated with ML models to recognize human faces and identify genders.

## Installation Instruction for MacOS
1. Install [Anaconda Python](https://www.anaconda.com/python-r-distribution?utm_campaign=alternatives&utm_medium=online-advertising&utm_source=google&utm_content=anaconda-download&gclid=Cj0KCQjw8uOWBhDXARIsAOxKJ2GDaAj3Zz6WKqIglzV2mPYsv9LMkquFQaXOPfyJL5AbDtOoU-NOxmEaAqOaEALw_wcB)
2. Install virtural environment
   ```
   python3 -m pip install --user virtualenv
   ```
3. Create virtual environment
   ```
   python3 -m venv flask
   ```
4. Activate virtual environment
   ```sh
   source flask/bin/activate
   ```
5. Install dependencies in requirement.txt
   ```
   pip install -r requirements.txt
   ```
6. Install OpenCV
   ```
   pip install opencv-python
   ```

## 11 Steps to Develop Face Recognition ML Model Pipeline
1. Read input image
2. Convert image to greyscale
3. Extract/Crop the face using haar cascase classifier
4. Data normalization (min max)
5. Resize image to (100,100)
6. Flatten image to (1x10000)
7. Subtract mean
8. Get the eigen image
9. Pass to ML model - SVM
10. Generate the prediction and score
11. Mark the output on the image

## Integrate to Falsk Web App
1. Install flask
   ```
   python3 -m pip install Flask
   ```
2. How to run the web app
   ```
   python main.py
   ```
3. Set the development mode
   ```
   export FLASK_ENV=development
   ```

## Deploy to Heroku
1. Create a [Heroku account](https://signup.heroku.com/)
2. Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli)
3. Create Procfile
   ```
   echo "web: gunicorn app:app" > Procfile
   ```
4. Install Gunicorn
   ```
   python3 -m pip install gunicorn
   ```
5. Install dependencies
   ```
   python3 -m pip freeze > requirements.txt
   ```
6. Create the application
   ```
   heroku create face-recognition-classify
   ```
7. Push
   ```
   git push heroku master
   ```
