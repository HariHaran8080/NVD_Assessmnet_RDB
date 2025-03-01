## NVD CVE API Project

This project is a web application that fetches and displays CVE (Common Vulnerabilities and Exposures) details using the NVD (National Vulnerability Database) API. It is built using **React** for the frontend, **Node.js with Express** for the backend, and **MySQL** for database storage.

## 📌 Project Structure

nvd-cve-api/
│── backend/# Node.js Express backend
│── frontend/# React Vite frontend
│── README.md# Project documentation
│── .env # Environment variables
│── database.sql # Database schema

## 🚀 Tech Stack

### **Frontend**
- React (Vite)
- Bootstrap (for UI)
- Axios (for API calls)

### **Backend**
- Node.js (Express)
- MySQL (for database storage)
- dotenv (for environment variables)
- cors (for Cross-Origin Resource Sharing)

### **Database**
- MySQL (with a dedicated user and password for security)

## ⚙️ Installation Steps

### **1️⃣ Clone the Repository**

git clone https://github.com/your-repo/nvd-cve-api.git
cd nvd-cve-api

2️⃣ Setup MySQL Database
Log into MySQL and run:

## sql
CREATE DATABASE nvd_cve_db;
CREATE USER 'nvd_user'@'localhost' IDENTIFIED BY 'YourSecurePassword';
GRANT ALL PRIVILEGES ON nvd_cve_db.* TO 'nvd_user'@'localhost';
FLUSH PRIVILEGES;

3️⃣ Configure Environment Variables
Create a .env file in the backend folder:
DB_HOST=localhost
DB_USER=nvd_user
DB_PASSWORD=YourSecurePassword
DB_NAME=nvd_cve_db
DB_PORT=3306

4️⃣ Install Dependencies
Backend
cd backend
npm install

Frontend
cd ../frontend
npm install
▶️ Running the Application

1️⃣ Start the Backend
cd backend
node server.js

2️⃣ Start the Fronten
cd ../frontend
npm run dev

## 📡 API Endpoints
Backend Routes
Method	Endpoint	Description
GET	/api/cves	Fetch all CVEs from MySQL
GET	/api/cves/:id	Fetch CVE by ID
POST	/api/cves	Add a new CVE entry
DELETE	/api/cves/:id	Delete a CVE entry

🛠️ Troubleshooting
1️⃣ MySQL Authentication Issue
If you see an error like:
ER_NOT_SUPPORTED_AUTH_MODE: Client does not support authentication protocol
Run this inside MySQL:
sql
ALTER USER 'nvd_user'@'localhost' IDENTIFIED WITH mysql_native_password BY 'YourSecurePassword';
FLUSH PRIVILEGES;

2️⃣ Port Issues
If MySQL (3306) is busy, change DB_PORT in .env.
If Frontend (Vite) or Backend (Node.js) ports conflict, update package.json scripts.

📌 Future Enhancements
✅ Improve UI/UX with better animations
✅ Implement search & filtering for CVEs
✅ Add user authentication for accessing the database





