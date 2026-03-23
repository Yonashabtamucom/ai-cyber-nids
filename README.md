## AI-Powered Network Intrusion Detection System (NIDS)

##  Project Overview
This project builds a Machine Learning-based Network Intrusion Detection System using the UNSW-NB15 dataset.  
The goal is to detect whether network traffic is **Normal (0)** or an **Attack (1)**.


##  Features
- Data preprocessing and cleaning
- Encoding categorical features (protocol, service, state)
- Machine learning model using Random Forest
- Feature importance analysis
- Performance evaluation (accuracy, precision, recall, F1-score)


## Dataset
- Dataset: UNSW-NB15
- Contains real network traffic with labeled attacks
- Features include:
  - Packet counts
  - Traffic rate
  - Timing (latency, inter-packet time)
  - Protocol and service types


##  Technologies Used
- Python
- Pandas
- Scikit-learn
- Matplotlib


##  Project Workflow
1. Load dataset to vs code
2. Drop target leakage features (`label`, `attack_cat`)
3. Encode categorical features (`proto`, `state`, `service`)
4. Align train and test datasets
5. Train Random Forest model
6. Evaluate performance
7. Analyze feature importance


## Model Performance

                precision   recall    f1-score  support

           0       0.96      0.73      0.83     37000
           1       0.82      0.97      0.89     45332

    accuracy                           0.87     82332
    macro avg       0.89      0.85      0.86     82332
    weighted avg       0.88      0.87      0.86     82332

 The model prioritizes detecting attacks (high recall), which is critical in cybersecurity.


##  Key Insights
- Most important features:
  - `ackdat`, `tcprtt`, `synack` → connection timing
  - `rate`, `sload`, `dload` → traffic intensity
  - `sbytes`, `dbytes` → data volume
- Behavioral patterns are more important than protocol type.

## Future Improvements
- Use XGBoost / Gradient Boosting
- Multi-class classification (attack types)
- Deploy using Streamlit
= Real-time network monitoring

 ## Author
YONAS HABTAMU
Data Science & Cybersecurity Student
