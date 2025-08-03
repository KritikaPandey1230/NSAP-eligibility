# 🤖 NSAP Scheme Eligibility Prediction using Machine Learning

> **"Technology, when combined with empathy, becomes a tool for transformation."**

This project applies Machine Learning to assist in social welfare distribution under India’s **National Social Assistance Programme (NSAP)**. The aim is to predict the most appropriate scheme for a beneficiary based on demographic and socio-economic data, using real government datasets and deploying the model on IBM Cloud.



## 🧠 Why This Project Matters

Thousands of citizens—elderly, widows, and persons with disabilities—rely on NSAP for survival. Manual verification is slow and often error-prone. This project builds an intelligent system to:
- **Reduce verification delays**
- **Ensure timely and fair allocation**
- **Improve transparency in governance**


## 📊 What This Project Does

- Analyzes real-world NSAP data from AI Kosh  
- Applies a **Random Forest classifier** for multi-class prediction  
- Automates scheme classification using features like:
  - State, district codes
  - Gender and caste breakdowns
  - Aadhaar and mobile number availability

- Deploys the model using:
  - **Jupyter Notebook** (manual training + visualization)
  - **IBM AutoAI** (automated pipeline generation + deployment)



## 🔍 Key Technologies

- **Languages:** Python  
- **Libraries:** pandas, NumPy, scikit-learn, seaborn, matplotlib  
- **Tools:** Jupyter Notebook, IBM Watson Studio, AutoAI  
- **Cloud Services:** IBM Cloud Object Storage, Watson Machine Learning  

---

## 🚀 How to Use This Project

### 🖥️ Locally

git clone https://github.com/your-username/nsap-scheme-eligibility.git
cd nsap-scheme-eligibility
pip install -r requirements.txt
jupyter notebook



###🌐 On IBM Cloud
Upload dataset to IBM Cloud Object Storage

Use Watson Studio / AutoAI to train and deploy the model

Consume model via REST API for real-time predictions

###📈 Results at a Glance
Model Used: Random Forest Classifier

Accuracy: ~96% on test set

Evaluation: Confusion Matrix, Classification Report, Feature Importance

Deployment: REST API hosted on IBM Cloud (AutoAI / WML)

###💡 Insights Gained
Feature importance revealed that Aadhaar linkage and gender/caste composition strongly affect scheme classification.

The use of AutoAI greatly accelerated model tuning and deployment.

This approach can be scaled to predict eligibility across other welfare schemes as well.

###🛤️ Future Enhancements
Build a secure web interface for government officers.

Integrate real-time applicant form input.

Explore advanced models like XGBoost or Neural Networks.

Expand coverage to additional districts and schemes.

###Screenshot
<img width="1909" height="883" alt="Screenshot 2025-07-27 183356" src="https://github.com/user-attachments/assets/6dde1737-2cdc-4357-a846-4162f7b7791f" />
<img width="1917" height="878" alt="Screenshot 2025-07-27 183421" src="https://github.com/user-attachments/assets/3333d708-eb34-450a-8393-69bf02b036a7" />
<img width="1913" height="730" alt="Screenshot 2025-07-27 183442" src="https://github.com/user-attachments/assets/83acc167-6e1e-439d-9129-a25a96751a85" />
<img width="1913" height="730" alt="Screenshot 2025-07-27 183442" src="https://github.com/user-attachments/assets/87e6ff8c-bef1-4686-9012-2e84c8a2c3c1" />
<img width="1915" height="879" alt="Screenshot 2025-07-27 183512" src="https://github.com/user-attachments/assets/1e9a59c6-7630-4841-b1c5-a058a13fc11b" />



###👩‍💻 Author
Kritika Pandey
Final Year B.Tech IT Student
Rajkiya Engineering College, Azamgarh
Aspiring Full-Stack & ML Developer | Government Tech Enthusiast

###📌 Final Thought
“Building solutions that touch lives is more than coding—it’s a contribution to society.”

If this project inspired you or helped you, give it a ⭐ and feel free to connect with me.








-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# NSAP Scheme Eligibility Prediction using IBM AutoAI

This project uses **IBM Watson AutoAI** to automatically build, train, and deploy a machine learning model that predicts the most suitable **NSAP scheme** for an applicant.

## 📌 Problem Statement

Predict which NSAP scheme a citizen qualifies for, using government data on demographics and socio-economic factors. Manual allocation is slow and prone to error—ML automates this efficiently.

## 🌐 Platform

- **IBM Watson Studio (AutoAI)**
- **IBM Cloud Object Storage**
- **Watson Machine Learning (Deployment)**

## 🧠 AutoAI Features Used

- Automated data cleaning
- Auto feature engineering
- Multiple model candidates (XGBoost, LGBM, Logistic Regression)
- Pipeline comparison and leaderboard
- Model deployment as REST API

## 📝 Dataset Info

- CSV file: `nsapallschemes.csv`
- Loaded from IBM Cloud Object Storage
- Columns include total beneficiaries, gender, caste categories, Aadhaar/mobile data, etc.

## 🚀 Deployment

- Model deployed as a REST API using Watson Machine Learning
- Used API Key and Access Token for secure authentication
- Integrated with Python requests to test predictions

## 🔄 API Request Example


payload_scoring = {
    "input_data": [{
        "fields": ["lgdstatecode", "lgddistrictcode", "totalbeneficiaries", "totalmale", ...],
        "values": [[18, 122, 5045, 2500, ...]]
    }]
}
response = requests.post(deployment_url, json=payload_scoring, headers=header)
print(response.json())


## Screenshot
<img width="1902" height="796" alt="Screenshot 2025-07-27 173221" src="https://github.com/user-attachments/assets/7049652c-e129-400d-9ea4-6f58e599f933" />
<img width="1919" height="869" alt="Screenshot 2025-07-27 174558" src="https://github.com/user-attachments/assets/2bcd349c-1c22-495a-9186-7bc97a2c4ada" />
<img width="1901" height="885" alt="Screenshot 2025-07-27 174614" src="https://github.com/user-attachments/assets/5233f779-c17f-40a5-8e45-09d490181096" />



