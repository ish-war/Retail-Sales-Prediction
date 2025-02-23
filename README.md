# 📊 Retail Sales Prediction

## Web Interface
![Screenshot 2025-02-23 162505](https://github.com/user-attachments/assets/db84174c-3b56-424d-aa3e-60bc952367bf)
![Screenshot 2025-02-23 162552](https://github.com/user-attachments/assets/dcc875e1-7d00-4447-915e-561798e86618)

## 📝 Overview
The **Retail Sales Prediction** project aims to develop a **machine learning model** that forecasts sales across retail stores using the **Rossmann dataset**. This project explores sales patterns, identifies key influencing factors, and provides actionable insights to optimize store performance. The complete workflow integrates **data preprocessing, feature engineering, model selection, and deployment** using **Docker and Minikube**.

## 🚀 Technologies Used
- **Python** (Data Processing & Machine Learning)
- **Pandas, NumPy, Matplotlib, Seaborn** (Data Cleaning & Visualization)
- **Scikit-Learn** (Model Training)
- **Streamlit** (Web Application)
- **Docker** (Containerization)
- **Kubernetes (Minikube)** (Deployment & Scaling)
- **Git & GitHub** (Version Control)

## 🔍 Approach
### 1️⃣ Data Collection & Preprocessing
- Loaded the datasets.
- Handled **missing values** and removed duplicates.
- Combined datasets for comprehensive analysis.
- Extracted **year, month, and day** from the `Date` variable.

### 2️⃣ Exploratory Data Analysis (EDA)
- Used multiple **visualizations** to explore relationships between variables.
- Identified **patterns** and formulated hypotheses.
- Analyzed key factors affecting sales such as **promotions, store types, and competition distance**.

### 3️⃣ Feature Engineering & Transformation
- Applied **one-hot encoding** on categorical variables.
- Removed **redundant** or highly correlated features.
- Scaled numerical features using **StandardScaler**.

### 4️⃣ Model Training & Evaluation
- Experimented with multiple models:
  - **Linear Regression**
  - **Decision Tree**
  - **RandomForest Regressor** ✅ (Best Performing Model)
- Evaluated models using:
  - **Root Mean Squared Error (RMSE)**
  - **R² Score**
- RandomForest Regressor showed the best balance between accuracy and overfitting.

### 5️⃣ Deployment & Containerization
- **Built a Streamlit app** to provide an interactive sales prediction tool.
- **Dockerized the application** for easy deployment.
- Used **Minikube & Kubernetes** for container orchestration.

## 📊 Key Insights & Findings
- **Promotions significantly boost sales**.
- **Store type 'B' has the highest average sales**, despite fewer stores.
- **School holidays show a slight increase in sales**.
- **Competition distance strongly influences sales trends**.

## ⚠️ Challenges & Limitations
- **Data Quality Issues**: Missing values and inconsistencies required careful handling.
- **External Factors**: Economic conditions, seasonal effects, and competitor strategies were not accounted for.
- **Generalization**: The model provides an overall forecast but may not be highly accurate for individual stores.

## 🔮 Future Enhancements
- **Incorporate external economic indicators** (inflation, GDP, etc.) to improve predictions.
- **Deploy a real-time model monitoring system**.
- **Experiment with deep learning models** (e.g., LSTMs for time-series forecasting).

## 🛠️ Project Setup & Execution
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/ish-war/retail-sales-prediction.git
cd retail-sales-prediction
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Streamlit App
```bash
streamlit run app.py
```

### 4️⃣ Build & Run with Docker
```bash
docker build -t retail-sales-prediction .
docker run -p 8501:8501 retail-sales-prediction
```

### 5️⃣ Deploy with Minikube
```bash
minikube start
minikube image load retail-sales-prediction
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
minikube service sales-app-service --url
```

## 📌 Folder Structure
```
📂 retail-sales-prediction
│── 📜 app.py                 # Streamlit application
│── 📜 model_building.ipynb    # Jupyter Notebook for model training
│── 📜 requirements.txt        # Dependencies
│── 📜 Dockerfile              # Docker configuration
│── 📜 deployment.yaml         # Kubernetes Deployment
│── 📜 service.yaml            # Kubernetes Service
│── 📜 .gitignore              # Files to ignore in GitHub
└── 📂 data                    # Raw dataset files
```

## 🤝 Contributing
Contributions are welcome! Feel free to open an **issue** or submit a **pull request**.

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

---
**🔗 Connect with me:** [My LinkedIn](https://www.linkedin.com/in/ishwar-ambad) | [GitHub](https://github.com/ish-war) 🚀

