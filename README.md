 
# 🧠 Intelligent Cycle Prediction App

A **Machine Learning web application** that predicts menstrual cycle length using health and demographic data. The application is built with **Python and Streamlit**, powered by **Random Forest regression**, containerized using **Docker** and deployed on **AWS EC2** with a live public demo.

You can access the live, running application here:
**[http://13.233.111.23:8501](http://13.233.111.23:8501)**

---

## 🚀 Project Overview

This project demonstrates how a real-world ML system is designed, built, deployed, and served to users. It supports both **personalized predictions** (user-specific models) and **generalized predictions** (new user inputs), making it suitable for healthcare, FemTech and applied ML use cases.

The application allows users to:
- Explore predictions for existing users from a real dataset
- Enter their own health data and receive cycle length predictions
- Interact with a clean, responsive UI
- Access the system via a cloud-hosted, containerized deployment

---

## ✨ Key Features

- End-to-end Machine Learning pipeline (data → model → prediction)
- Random Forest regression for cycle length prediction
- Personalized user-specific modeling
- General model for new/manual user inputs
- Automatic BMI calculation
- Interactive Streamlit-based UI
- Dockerized for reproducible deployment
- Live deployment on AWS EC2

---

## 🧠 Machine Learning Details

- **Model Used:** RandomForestRegressor  
- **Target Variable:** Length of menstrual cycle (days)  

### Input Features
- Age  
- Cycle Number  
- Height, Weight, BMI  
- Years Married, Years of Schooling  
- Number of Pregnancies, Living Children  
- Luteal Phase Length  
- Total Menses Score  

### Model Strategy
- A **general model** trained on the full dataset for new users
- **User-specific models** trained dynamically for users with sufficient history
- Missing values handled using **median imputation**
- Performance evaluated using **Out-of-Bag (OOB) score**

---

## 🖥️ Application Modes

### Mode 1: Explore Predictions for Existing Users
- Select a user ID from the dataset
- A personalized model is trained for that user
- Predicts the next cycle length
- Displays predicted vs actual values and accuracy score

### Mode 2: Predict Using Manual User Input
- Users enter their own health and cycle information
- BMI is calculated automatically
- A general ML model predicts the next cycle length

---

## 🐳 Docker & Deployment

The application is containerized using Docker to ensure consistent behavior across environments.

### Docker Highlights
- Lightweight Python base image
- Dependencies managed via `requirements.txt`
- Streamlit server exposed on port `8501`

### Cloud Deployment
- Deployed on **AWS EC2**
- Public IP access enabled
- Application runs as a long-lived service

---

## 📂 Project Structure
```

Intelligent Cycle Prediction App/
│
├── app.py                       # Model + Streamlit application
├── Dockerfile                   # Docker configuration
├── requirements.txt             # Python dependencies
├── FedCycleData071012.csv       # Dataset
├── .gitignore                   # Git ignore rules
└── README.md                    # Project documentation
```

---

## ⚙️ How to Run Locally

### 1. Clone the Repository

```bash
git clone <repository-url>
cd intelligent-cycle-prediction-app
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Application

```bash
streamlit run app.py
```

The app will be available at:

```
http://localhost:8501
```

---

## 🐳 Run with Docker

### Build Docker Image

```bash
docker build -t cycle-predictor .
```

### Run Container

```bash
docker run -p 8501:8501 cycle-predictor
```

---

## 🎯 Use Cases

* FemTech & digital health platforms
* Applied machine learning systems
* Cloud-based ML deployment demos
* DevOps + ML (MLOps) portfolio project
* Academic major / capstone project

---

## 🔮 Future Improvements

* Add model explainability (SHAP / feature importance)
* Store prediction history in a database
* Add CI/CD pipeline for automated deployment
* Enable secure authentication for users
* Integrate real-time health APIs

---

## ⚠️ Disclaimer

This application is for **educational and research purposes only**. It is not intended to provide medical advice or replace consultation with healthcare professionals.

---

## 👤 Author

**Motapothula Sai Karthik** \
B.Tech CSE \
saikarthikmotapothula333@gmail.com

## 🛠️ Tech Stack

- **Backend:** Python, Pandas, Scikit-learn
- **Frontend:** Streamlit
- **Containerization:** Docker
- **Deployment:** AWS EC2
