## **Credit Card Fraud Detection System**

---

### **Problem Solved**
- Built a **machine learning system** to detect fraudulent credit card transactions  
- Achieved **86–92% fraud detection accuracy**  
- Designed to **minimize customer disruption** while maintaining strong fraud coverage  

---

### **Dataset**
- **Source:** Kaggle  
- **Total Transactions:** **284,807** real-world records  
- **Fraud Rate:** **0.172%** (492 fraud cases) → *extreme class imbalance*  

**Features:**
- 30 anonymized features  
- Time  
- Amount  

**Target Variable:**
- `0` → Normal Transaction  
- `1` → Fraudulent Transaction  

---

### **Technical Implementation**

#### **Preprocessing**
- Applied **RobustScaler** to **Time** and **Amount** features  
- Ensured stability against outliers  

#### **Imbalance Handling**
- **SMOTE (Oversampling)** for minority class  
- **Undersampling** for majority class  
- Balanced precision–recall tradeoff  

---

### **Models Trained**
- Logistic Regression  
- **Random Forest → Best Performer**  
- Support Vector Machine (SVM)  
- Isolation Forest *(unsupervised baseline)*  

---

### **Key Results**

| **Model** | **Fraud Caught** | **False Alarms (Precision)** | **AUC-ROC** | **Decision** |
|---------|-----------------|------------------------------|------------|-------------|
| **Random Forest** | **86%** | **45%** | **0.983** | **Recommended** |
| Logistic Regression | 92% | 6% | 0.971 | Too many false alerts |
| SVM | 92% | 5% | 0.974 | Too many false alerts |

---

### **Business Impact**
- **Money Saved:** **$20,531** per **98 fraud cases**  
- **ROI:** **300% return on investment**

**Customer Impact:**
- **80% reduction in false alarms** compared to other models  

**Operational Efficiency:**
- **50 alerts/day per 100K transactions**  
- *(vs 250–285 alerts/day from other models)*  

---

### **Deployment Readiness**
- Models saved as **`.joblib` files**  
- **Prediction API function** implemented  
- **Risk Classification:** HIGH / MEDIUM / LOW  
- Supports **real-time transaction scoring**  
- Includes **business metrics calculator**  

---

### **Why Random Forest Wins**
- **Best balance:**  
  - Catches **86% of fraud** with manageable false alarms  
- **Financially viable:**  
  - Positive ROI *(other models result in negative ROI due to alert overload)*  
- **Customer-friendly:**  
  - Minimal blocking of legitimate transactions  
- **Production-ready:**  
  - Fast inference  
  - Interpretable feature importance  

---

### **For Detailed Analysis**
- **Complete Methodology:** Pages **3–5** of report  
- **Business Impact Calculations:** Pages **6–7**  
- **Deployment Architecture:** Pages **8–9**  
- **Full Results Comparison:** **Appendix A**
