# 🌞 Solar Farm Site Suitability Analysis with GIS & Machine Learning

## 🔰 Badges

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![GIS](https://img.shields.io/badge/GIS-008000?logo=qgis&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![GeoPandas](https://img.shields.io/badge/GeoPandas-43B02A?logo=geopandas&logoColor=white)
![Rasterio](https://img.shields.io/badge/Rasterio-FF6F00)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-4B8BBE)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-FF5722?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-2965f1?logo=css3&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?logo=visualstudiocode&logoColor=white)
![License](https://img.shields.io/badge/License-GPL--3.0-blue)

---

## 📌 What This Project Entails
This project identifies the most suitable locations for establishing **solar power farms** using **Geographic Information Systems (GIS)** and **Machine Learning**. It integrates spatial datasets, performs geospatial processing, and applies predictive modeling to assess land suitability based on environmental, geographic, and infrastructural factors.

---

## 🧠 Project Overview & Objectives

### 🎯 Objectives
- Analyze geographic, climatic, and infrastructural features influencing solar viability  
- Perform **spatial suitability analysis**  
- Build **Machine Learning models** to predict land suitability  
- Compare **Regression** and **Classification** approaches  
- Visualize insights and deploy results using a web interface  

---

## ❓ Problem Statement
Developing solar farms requires identifying optimal locations considering environmental safety, accessibility, radiation potential, terrain characteristics, and land-use constraints. Traditional manual evaluation is costly and inefficient. This project automates the suitability assessment using GIS data processing and ML models to **accurately recommend best-fit locations** for solar development.

---

## 🔄 Machine Learning Workflow
1. Data Collection & Integration (Raster and Vector data)  
2. Spatial Preprocessing & Cleaning  
3. Feature Engineering  
4. Regression Modeling  
5. Classification Modeling  
6. Model Evaluation  
7. Visualization & Insight Generation  
8. Deployment  

---

## 🗂️ Data Overview
The dataset includes spatial and tabular features related to:
- Solar radiation  
- Elevation, Terrain & Slope  
- Land Use / Land Cover  
- Administrative boundaries  

**Data Formats Used**
- Raster datasets (GeoTIFF)  
- Vector datasets (Shapefiles / GeoJSON)  

---

## 🔍 Exploratory Data Analysis (EDA)

### 🌍 Spatial Analysis
- Raster visualization  
- Spatial overlay analysis  

### 📊 Descriptive / Statistical Analysis
- Distribution of key variables  
- Correlation analysis  


### 📊 Visuals 

<img width="428" height="529" alt="image" src="https://github.com/user-attachments/assets/5cb968d1-1a65-4609-a86a-5783cfd1b8a7" />

<img width="861" height="984" alt="image" src="https://github.com/user-attachments/assets/eaea484a-9835-4891-ab6f-a152bf0006b0" />

<img width="784" height="384" alt="image" src="https://github.com/user-attachments/assets/ca3cd2c9-2106-46f7-90d7-42ea896902a6" />

<img width="640" height="529" alt="image" src="https://github.com/user-attachments/assets/e155ea8e-7e06-4f62-beb3-c61772d012fc" />

### Key Insights 

- This map visualizes the spatial distribution of photovoltaic (PV) power output potential across Kenya.

- Warmer colors (yellow–red) represent higher solar potential,

- Cooler tones (green–blue) denote lower PV output.

- The correlation heatmap shows pairwise relationships between resource layers. High correlation between GHI, GTI, and PVOUT is expected since PVOUT derives from irradiance; this indicates redundancy.


---

## 🤖 Modeling Approach

### 1️⃣ Regression Modeling

- The regression approach predicts  **PVOUT** for each location based on multiple environmental and infrastructural variables.

- Model used is the Random Forest Regressor

**Metrics Evaluated**
- R² Score  
- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)  

---

### 2️⃣ Classification Modeling
The classification approach categorizes each area into suitability classes:
- Highly Suitable  
- Moderately Suitable  
- Low Suitability  
- Unsuitable  

**Algorithms Used**
- Random Forest Classifier  
- Gradient Boosting / XGBoost (if used)  

---

## 📈 Performance & Evaluation

### ✅ Regression Evaluation
- R² Score -  0.99
- RMSE - 1.46
- MAE  -  0.45

### ✅ Classification Evaluation
- Accuracy  - 0.99
- Precision / Recall / F1-score  - 0.99


---

## 🖼️ Visualizations

### 📌 Confusion Matrix  

<img width="610" height="473" alt="image" src="https://github.com/user-attachments/assets/1a2327b1-e720-463f-9b34-fe0792b9479c" />


### 📌 Actual vs Predicted Values  

<img width="784" height="584" alt="image" src="https://github.com/user-attachments/assets/e8d44227-887b-49b0-9b25-e381ee5133a1" />


---

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/kennethnyangweso/Solar-Farm-Site-Suitability-Analysis-with-GIS-and-Machine-Learning
cd Solar-Farm-Site-Suitability-Analysis-with-GIS-and-Machine-Learning

# Create virtual environment
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\\Scripts\\activate    # Windows

# Install dependencies
pip install -r requirements.txt
```

## 🚀 Deployment

### 📜  Model Deployment Procedure (Flask + React + Tailwind CSS)

1. Overview

- This deployment setup serves two separate models — one for regression (PVOUT prediction) and another for classification (site suitability) — using a Flask backend for the APIs and a React + Tailwind CSS frontend for visualization and interaction.

2. Backend Setup (Flask API)

- Create and activate a Python virtual environment.

- Install all necessary Python dependencies (Flask, Flask-CORS, Pandas, Numpy, Joblib, Scikit-learn).

- Load the trained regression or classification model (.pkl file).

- Define an API endpoint (/predict) that receives input features and returns model predictions in JSON format.

- Test the API locally using http://127.0.0.1:5000/.

- Confirm the API responds correctly with a sample prediction.

- Each model (regression and classification) runs as a separate Flask app, each listening on its own port (e.g., 5000 for regression and 5001 for classification).

3. Frontend Setup (React + Tailwind)

- Create a new React project using create-react-app.

- Install Tailwind CSS, PostCSS, and Autoprefixer for styling.

- Configure Tailwind by updating the content paths and adding base, components, and utilities layers in index.css.

- Install Axios for API communication.

- Create React components for:

- RegressionForm → communicates with the regression Flask API.

- ClassificationForm → communicates with the classification Flask API.

- Use Axios to send POST requests to the backend APIs with user inputs.

- Display prediction results dynamically in the frontend interface.

- Test the frontend at http://localhost:3000 and ensure successful communication with Flask.

4. Connecting Frontend and Backend

- Enable CORS in the Flask backend to allow requests from the React frontend.

- Update the Axios request URLs in the React app to match the backend server address (e.g., http://127.0.0.1:5000/predict).

- Test the full workflow:

- Start Flask (python backend_regression.py).

- Start React (npm start).

- Input sample data and confirm predictions appear on the dashboard.

▶️ Usage

    python main.py

```bash
# Run Flask backend
python app.py

# Run React frontend
npm install
npm start

```

## 🖥️ Results
<img width="1355" height="614" alt="React App - Google Chrome 11_11_2025 1_36_42 PM" src="https://github.com/user-attachments/assets/00b9eedd-0249-42c4-8e70-784e79cdeb32" />

<img width="1351" height="605" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/afa21713-679a-477e-8968-9cf0ce8db80e" />

---

## 💡 Future Improvements

- Include additional geospatial variables

- Integrate satellite time-series analysis

- Deploy on cloud platforms

## 🤝 Contributions

Contributions are welcome! Feel free to fork, enhance, and submit a pull request.

## 🙌 Acknowledgment

Special thanks to the open-source GIS and Machine Learning community.

## 👨‍💻 Author

**Kenneth Nyangweso**  
Data Scientist | GIS & Machine Learning Engineer  

🔗 GitHub: [kennethnyangweso](https://github.com/kennethnyangweso)  
