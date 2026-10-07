# 🏡 Bangalore House Price Prediction

### Machine Learning-Based Real Estate Price Estimation

**Bangalore House Price Prediction** is a full-stack machine learning application that estimates residential property prices in Bangalore based on features such as **location, total square footage, number of bedrooms, and bathrooms**.

The project combines a **Scikit-learn machine learning model**, **Flask REST API**, and a lightweight **HTML/CSS/JavaScript frontend** to provide an interactive house price prediction experience.

> **Core Objective:** Build an end-to-end machine learning application that transforms real-world housing data into an accessible property price prediction tool.

---

## 🚀 Key Features

- 🏠 **House Price Prediction** — Estimate property prices based on user-provided housing features.
- 📍 **Location-Based Prediction** — Incorporates Bangalore locality information into the prediction.
- 📐 **Property Feature Analysis** — Uses square footage, BHK, and bathroom count as prediction features.
- 🌐 **Web Interface** — Interactive frontend built with HTML, CSS, and JavaScript.
- ⚡ **REST API** — Flask backend exposes the trained model for real-time predictions.
- 🤖 **Machine Learning Model** — Model trained using Scikit-learn and real-world housing data.
- 🧩 **Modular Architecture** — Separates the frontend, backend, dataset, and model-training components.

---

# 🏗️ System Architecture

```text
┌────────────────────────────────────┐
│          Web Frontend              │
│                                    │
│  HTML + CSS + JavaScript           │
│                                    │
│  Location                          │
│  Square Feet                       │
│  BHK                               │
│  Bathrooms                         │
└──────────────────┬─────────────────┘
                   │
                   │ HTTP Request
                   ▼
┌────────────────────────────────────┐
│           Flask API                │
│                                    │
│  server.py                         │
│  util.py                           │
│                                    │
│  Request Validation                │
│  Feature Processing                │
│  Model Inference                   │
└──────────────────┬─────────────────┘
                   │
                   ▼
┌────────────────────────────────────┐
│       Trained ML Model             │
│                                    │
│  Scikit-learn                     │
│  Serialized Model                 │
│                                    │
│  house features → price           │
└──────────────────┬─────────────────┘
                   │
                   ▼
          Predicted House Price
```

---

# 🧠 Machine Learning Pipeline

```text
Raw Housing Dataset
        │
        ▼
Data Cleaning & Preprocessing
        │
        ▼
Feature Engineering
        │
        ▼
Model Training
        │
        ▼
Model Evaluation
        │
        ▼
Model Serialization
        │
        ▼
Flask API
        │
        ▼
Web Application
        │
        ▼
House Price Prediction
```

---

# 📊 Input Features

The prediction model uses the following property characteristics:

| Feature | Description |
|---|---|
| **Location** | Bangalore property locality |
| **Total Square Feet** | Size of the property |
| **BHK** | Number of bedrooms |
| **Bathrooms** | Number of bathrooms |

### Example Input

```text
Location: Whitefield
Total Square Feet: 1200
BHK: 2
Bathrooms: 2
```

### Output

```text
Estimated House Price: ₹XX Lakhs
```

---

# 🤖 Model

The project uses a **Scikit-learn regression model** trained on Bangalore housing data.

### Model Components

- **Pandas** — Data loading and manipulation
- **NumPy** — Numerical operations
- **Scikit-learn** — Machine learning and preprocessing
- **Pickle** — Model serialization

The trained model is stored as:

```text
server/artifacts/bangalore_home_prices_model.pickle
```

Feature/column metadata is stored in:

```text
server/artifacts/columns.json
```

> **Note:** The original project description mentions Linear Regression, Random Forest, or Ridge depending on the model used. The exact trained algorithm should be specified here based on the final model in `model_training.ipynb`.

---

# 🛠️ Technology Stack

## 🤖 Machine Learning

| Technology | Purpose |
|---|---|
| **Python** | ML and backend development |
| **Pandas** | Data processing |
| **NumPy** | Numerical computation |
| **Scikit-learn** | Model training and prediction |
| **Jupyter Notebook** | Model development and experimentation |

## ⚙️ Backend

| Technology | Purpose |
|---|---|
| **Flask** | REST API |
| **Python** | Backend runtime |

## 🎨 Frontend

| Technology | Purpose |
|---|---|
| **HTML** | Page structure |
| **CSS** | Styling and layout |
| **JavaScript** | User interaction and API communication |

---

# 📁 Project Structure

```text
bangalore-house-price-prediction/
│
├── client/
│   ├── app.html
│   ├── app.css
│   └── app.js
│
├── server/
│   ├── server.py
│   ├── util.py
│   │
│   └── artifacts/
│       ├── bangalore_home_prices_model.pickle
│       └── columns.json
│
├── data/
│   └── bangalore_home_prices.csv
│
├── model/
│   └── model_training.ipynb
│
└── README.md
```

---

# 🔄 Application Workflow

```text
User
 │
 │ Enters property details
 ▼
Frontend
 │
 │ HTTP Request
 ▼
Flask API
 │
 │ Preprocess features
 ▼
Trained ML Model
 │
 │ Generate prediction
 ▼
Flask API
 │
 │ JSON Response
 ▼
Frontend
 │
 ▼
Display Estimated Price
```

---

# 🚀 Getting Started

## Prerequisites

Make sure you have:

- Python 3.9+
- pip
- Jupyter Notebook
- A modern web browser

---

## ⚙️ Backend Setup

Navigate to the server directory:

```bash
cd server
```

Create a virtual environment:

```bash
python -m venv venv
```

### macOS / Linux

```bash
source venv/bin/activate
```

### Windows

```bash
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install flask pandas numpy scikit-learn
```

Start the Flask server:

```bash
python server.py
```

The API will typically run at:

```text
http://127.0.0.1:5000
```

---

# 🌐 Running the Frontend

Navigate to the client directory:

```bash
cd client
```

Open:

```text
app.html
```

in your browser.

The frontend collects the property details and communicates with the Flask backend to retrieve the predicted house price.

---

# 🧪 Model Development

The model development workflow is contained in:

```text
model/model_training.ipynb
```

The notebook can be used to:

1. Load the Bangalore housing dataset.
2. Explore and clean the data.
3. Preprocess housing features.
4. Encode location information.
5. Train the regression model.
6. Evaluate model performance.
7. Serialize the trained model.
8. Export the feature metadata used by the Flask API.

---

# 📈 Example Prediction

```text
Property Details
────────────────────────────
Location      → Whitefield
Square Feet   → 1,200
BHK           → 2
Bathrooms     → 2
────────────────────────────

             ↓

       Machine Learning
             ↓

    Estimated Property Price
```

---

# 💡 Key Concepts Demonstrated

This project demonstrates practical experience with:

- Supervised machine learning
- Regression problems
- Real-world tabular data
- Data preprocessing
- Feature engineering
- Categorical feature handling
- Model training and evaluation
- Model serialization
- REST API development
- Flask
- Frontend/backend integration
- End-to-end ML application development

---

# 🔮 Future Improvements

Potential extensions include:

- [ ] Compare multiple regression algorithms
- [ ] Hyperparameter optimization
- [ ] Cross-validation
- [ ] Model performance dashboard
- [ ] Interactive price visualization
- [ ] Additional property features
- [ ] Neighborhood-level market analysis
- [ ] Automated model retraining
- [ ] Cloud deployment
- [ ] Responsive mobile UI

---

## 👩‍💻 Author

**Pratheksha Kanagaraj**

Computer Science Graduate Student · Software Engineer · AI/ML Enthusiast

---

⭐ **If you found this project useful, consider giving the repository a star!**
