# 🚀 Automated ETL Pipeline using Apache NiFi

A video demonstration showcasing the project workflow is available:  
📹 **[Watch Demo Video](https://drive.google.com/file/d/1XwSoJgIVOpUqbz5IiXWKX8hdIpaCBR2q/view?usp=sharing)**

---

## 📄 Project Overview
This project aims to automate the ETL (Extract, Transform, Load) pipeline using **Apache NiFi**. The solution integrates dynamic database configurations, LLM-based data transformation, and a frontend interface for seamless user interaction.

### 🌟 Key Features
- **Automated ETL Pipeline:** NiFi automates data extraction, transformation, and loading.
- **Dynamic Database Support:** Users can specify source and target database credentials directly from the frontend.
- **AI-Driven Transformation:** Integrated with **Gemini API** to dynamically enhance data transformation logic.
- **Frontend Integration:** Developed a web-based UI (hosted via Vercel) for easy user interaction.

---

## 🛠️ Technologies Used
- **Apache NiFi 2.3.0** (Core ETL Automation)
- **Google Gemini API (v2.2)** (LLM Integration for data transformation)

---

## 📋 Pipeline Flow Structure
```
HandleHttpRequest → EvaluateJsonPath → UpdateAttribute → ExecuteSQL → SplitRecord → InvokeHTTP (Gemini API) → MergeContent → PutDatabaseRecord → HandleHttpResponse
```

---

## 🚀 How to Run the Project
### Step 1: Start Apache NiFi
1. Navigate to your NiFi installation directory.
2. Run the following command to start NiFi:
```
./bin/nifi.cmd start
```
3. Access the NiFi UI at **https://localhost:8443**.


## 📧 Contact
For queries or assistance, please reach out via email or GitHub discussions. 😊

