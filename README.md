🛰 ColideX: Hybrid AI System for Space Debris Collision Prediction

ColideX is an AI-powered Space Situational Awareness (SSA) system designed to predict potential collisions between operational satellites and orbital debris. The system integrates real-time orbital data from Space-Track.org, a physics-based propagation model (SGP4), and advanced machine learning techniques (LSTM + Random Forest) to deliver accurate collision risk predictions and trajectory forecasting.

🚀 Key Features
Real-time orbital data integration using Space-Track API
Physics-based trajectory prediction using SGP4
Time-series trajectory refinement using LSTM
Collision probability prediction using Random Forest
Risk classification: Low / Medium / High
Automated feature engineering from orbital parameters
Hybrid AI architecture combining physics + deep learning + ML
Decision-support insights for satellite safety
🎯 Project Objectives

The system aims to:

Predict satellite–debris collision probability
Forecast future orbital trajectories using hybrid modeling
Improve trajectory accuracy beyond traditional physics models
Classify collision risk levels for decision-making
Enable proactive space situational awareness
🧠 Hybrid Model Architecture
🔹 Pipeline Overview
Space-Track API (TLE Data)
        ↓
SGP4 (Orbit Propagation - Physics Layer)
        ↓
Trajectory Data (Position & Velocity)
        ↓
LSTM (Time-Series Learning Layer)
        ↓
Refined Future Trajectory
        ↓
Feature Engineering
(distance, relative velocity, time-to-closest approach)
        ↓
Random Forest (Decision Layer)
        ↓
Collision Probability + Risk Classification
⚙️ System Components
🛰 SGP4 – Physics Layer
Converts TLE data into satellite/debris trajectories
Provides position and velocity vectors
Acts as the baseline deterministic model
Not trainable (physics-based)
🤖 LSTM – Temporal Intelligence Layer
Learns sequential motion patterns from trajectory data
Captures dynamic variations (drag, perturbations)
Improves future position prediction beyond SGP4
🌳 Random Forest – Decision Layer
Uses engineered features to predict collision risk
Outputs:
Collision probability score
Risk classification (Low / Medium / High)
📊 Model Outputs
Collision Probability Score (0–1)
Risk Classification: Low / Medium / High
Future Position Coordinates: (x, y, z)
Example:
Collision Probability: 0.82
Risk Level: HIGH
Future Coordinates: (4213, -1287, 5320)
📥 Data Sources
🔹 Primary Source
Space-Track.org API
TLE (Two-Line Element sets)
CDM (Conjunction Data Messages)
Satellite catalog data
🔹 Additional Sources
CelesTrak (public TLE datasets)
ESA DISCOS (object physical properties)
Kaggle datasets (ML training support)
🔄 Data Pipeline
Fetch Data (Space-Track API)
        ↓
Parse TLE Data
        ↓
SGP4 Propagation
        ↓
Generate Trajectory Dataset
        ↓
Train LSTM (trajectory prediction)
        ↓
Feature Engineering
        ↓
Train Random Forest (risk prediction)
        ↓
Prediction & Risk Scoring
▶️ Usage
🔹 Step 1: Fetch Data
python fetch_tle.py
🔹 Step 2: Train Models
python train_lstm.py
python train_rf.py
🔹 Step 3: Run Prediction
python predict.py
📈 Evaluation Metrics
Accuracy
Precision
Recall
F1-score
ROC-AUC
RMSE (trajectory prediction for LSTM)
Miss-distance estimation error
🧪 Algorithms Used
🔹 Physics-Based Model
SGP4 (Orbit Propagation)
🔹 Machine Learning Model
Random Forest (Collision Risk Prediction)
🔹 Deep Learning Model
LSTM (Trajectory Prediction)
🔹 Final Hybrid Model

👉 SGP4 + LSTM + Random Forest

🌍 Applications
Satellite mission planning
Collision avoidance systems
Space situational awareness platforms
Aerospace risk analytics
AI-based orbital prediction research
🔮 Future Enhancements
Transformer-based trajectory prediction
Real-time streaming from Space-Track API
3D orbital visualization (CesiumJS / Three.js)
Automated retraining pipeline
Collision avoidance maneuver simulation
Deployment as an interactive web dashboard
👨‍💻 Contributors

Developed as part of a Data Science / AI capstone project integrating orbital mechanics, deep learning, and machine learning to enhance satellite safety and mitigate risks caused by space debris.
