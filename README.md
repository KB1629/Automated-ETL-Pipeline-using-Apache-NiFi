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
- **Node.js + Express.js** (Backend Integration)
- **React (Vercel-hosted)** (Frontend Interface)
- **PostgreSQL**, **MSSQL**, and **MySQL** (Supported Databases)
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
./bin/nifi.sh start
```
3. Access the NiFi UI at **https://localhost:8443**.

### Step 2: Update NiFi Processors
- In `ExecuteSQL` and `PutDatabaseRecord`, update the database properties with:
```
Database Connection URL → ${db.source.url}  
Username → ${db.source.username}  
Password → ${db.source.password}  
```

### Step 3: Start the Backend Server
1. Navigate to your backend folder.
2. Run the following commands:
```
npm install
npm start
```

### Step 4: Start the Frontend
1. Navigate to your frontend folder.
2. Run the following commands:
```
npm install
npm run dev
```
3. Access the frontend at **http://localhost:3000**.

### Step 5: Testing the Pipeline
- Enter source and destination database details in the frontend form.
- Click **Start Pipeline** to trigger the workflow.
- Check NiFi UI for data flow status and metrics.

---

## ❗ Known Issues / Troubleshooting
- **Port Conflict:** Ensure no other service is running on port **8443** or **8089** before starting NiFi.
- **API Token Error:** If authentication fails, generate a new token from the NiFi UI's **Access Tokens** section.
- **Large Data Errors:** For datasets exceeding Gemini API limits, batch processing using `SplitRecord` and `MergeContent` is implemented.

---

## 📧 Contact
For queries or assistance, please reach out via email or GitHub discussions. 😊

