# 🏡 Bangalore Home Price Prediction

This project predicts the estimated home prices in Bangalore based on various input features such as location, square footage, number of bedrooms (BHK), and bathrooms.  
It uses a **Machine Learning model** trained on real housing data and provides a **web interface** built with HTML, CSS, and JavaScript, backed by a **Flask API**.

---

## 🚀 Features

- Predict house price instantly based on user inputs.
- Interactive frontend with modern UI.
- Flask backend serving predictions through REST API.
- ML model trained using Scikit-learn.
- Modular structure (separate `client`, `server`, and `model` components).

---

## 🏗️ Project Structure

Bangalore_Home_Price_Prediction/
│
├── client/
│ ├── app.html
│ ├── app.css
│ └── app.js
│
├── server/
│ ├── server.py
│ ├── util.py
│ ├── artifacts/
│ │ ├── bangalore_home_prices_model.pickle
│ │ └── columns.json
│
├── data/
│ └── bangalore_home_prices.csv
│
├── model/
│ └── model_training.ipynb
│
└── README.md



## 🚀 Model Details

- Algorithm: Linear Regression (or RandomForest / Ridge depending on your model)

- Libraries: Pandas, NumPy, Scikit-learn

- Input Features:

   - Total Square Feet

   - Location

   - Number of Bedrooms (BHK)

   - Number of Bathrooms
     
     

## 🚀 Technologies Used

- Frontend: HTML, CSS, JavaScript

- Backend: Python Flask

- Machine Learning: Scikit-learn, Pandas, NumPy

- Deployment (optional): Render / Heroku / AWS
