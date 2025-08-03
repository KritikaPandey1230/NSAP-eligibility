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



#### 🌐 On IBM Cloud
- Upload the dataset to **IBM Cloud Object Storage (COS)**.  
- Use **IBM Watson Studio AutoAI** to automatically build, test, and select the best model pipeline.  
- Alternatively, run the Jupyter notebook in **Watson Studio Notebook environment** for manual model development.  
- Deploy the final model using **Watson Machine Learning (WML)** as a REST API.  
- Test predictions using a Python `requests` script or directly via the IBM Cloud interface.

---

## 📈 Results at a Glance

- **Model Used:** Random Forest Classifier  
- **Accuracy:** ~96% on test dataset  
- **Evaluation Metrics:**  
  - Classification Report  
  - Confusion Matrix  
  - Feature Importance Chart  
- **Deployment:**  
  - REST API endpoint generated via Watson Machine Learning  
  - Model available for real-time predictions with proper input formatting

---

## 💡 Insights Gained

- **Aadhaar linkage** and **mobile number presence** are strong indicators of scheme classification.  
- Model performs reliably across various districts and scheme codes.  
- AutoAI enabled rapid model building, evaluation, and version tracking with minimal manual tuning.  
- Combining domain data with ML makes government scheme delivery more efficient.

---

## 🛤️ Future Enhancements

- Enable real-time form inputs through a web dashboard.  
- Use advanced models like Gradient Boosting or XGBoost for improved accuracy.  
- Integrate APIs with mobile apps for field-level access by officials.  
- Scale the system to other government schemes and additional states.  
- Explore Edge AI for low-connectivity rural areas.

---

## 📚 References

- [AI Kosh NSAP Dataset](https://aikosh.indiaai.gov.in)  
- [NSAP Official Portal](https://nsap.nic.in)  
- [Scikit-learn Documentation](https://scikit-learn.org)  
- [IBM Watson Studio](https://www.ibm.com/cloud/watson-studio)  
- [Watson Machine Learning](https://www.ibm.com/cloud/machine-learning)

---

## 👩‍💻 Author

**Kritika Pandey**  
Final Year B.Tech IT Student  
Rajkiya Engineering College, Azamgarh  
Aspirant | Full Stack Developer | ML Enthusiast  

---



## 📌 Final Thought

> “Machine learning isn’t just about accuracy — it’s about impact. When used for social good, even a line of code can change lives.”

If this project helped or inspired you, please ⭐ star the repo and share your feedback.  
Let's build tech that matters. 💙

---

###Screenshot
<img width="1909" height="883" alt="Screenshot 2025-07-27 183356" src="https://github.com/user-attachments/assets/6dde1737-2cdc-4357-a846-4162f7b7791f" />
<img width="1917" height="878" alt="Screenshot 2025-07-27 183421" src="https://github.com/user-attachments/assets/3333d708-eb34-450a-8393-69bf02b036a7" />
<img width="1913" height="730" alt="Screenshot 2025-07-27 183442" src="https://github.com/user-attachments/assets/83acc167-6e1e-439d-9129-a25a96751a85" />
<img width="1913" height="730" alt="Screenshot 2025-07-27 183442" src="https://github.com/user-attachments/assets/87e6ff8c-bef1-4686-9012-2e84c8a2c3c1" />
<img width="1915" height="879" alt="Screenshot 2025-07-27 183512" src="https://github.com/user-attachments/assets/1e9a59c6-7630-4841-b1c5-a058a13fc11b" />



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



