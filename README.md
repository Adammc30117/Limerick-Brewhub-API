# Limerick Brewhub API

A Spring Boot backend API for managing and analyzing craft beer reviews, breweries, and customer engagement across the EMEA region. Built for academic evaluation and portfolio demonstration.
---
## 🚀 Features
* **Task 1:** Customer summaries and brewery PDF reports with JSON, XML, and TSV responses
* **Task 2:** Add/update beer reviews, prevent duplicates, auto-update average ratings
* **Task 3:** Generate a detailed analytics PDF + QR code linking to the report hosted on GitHub
---
## 📦 Tech Stack
* Java 17, Spring Boot
* Spring Data JPA & MySQL
* JWT Security (Login, Logout, Refresh)
* Apache PDFBox, ZXing, JFreeChart
* Postman (for testing)
---
## 🔧 Setup Instructions
1. **Install Required Tools:**
   * Java 17+
   * Maven
   * IntelliJ IDEA (or any Java IDE)
   * XAMPP (for Apache + MySQL)
2. **Start XAMPP Services:**
   * Launch XAMPP Control Panel
   * Start **Apache** and **MySQL**
   * Open **phpMyAdmin** at: http://localhost/phpmyadmin
3. **Create MySQL Database:**
   * Name it: `beerdb`
   * Import SQL file from:
     `src/main/resources/static/assets/postman-sql_commands/beerdb.sql`
4. **Configure Database Connection:**
   Edit `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/beerDB
spring.datasource.username=root
spring.datasource.password=your_password
```
5. **Run in IntelliJ:**
   * Open the project folder
   * Right-click `AssignmentOneStarterApplication.java` → Run
---
## 🧪 Testing with Postman
Use the SQL + Postman command notes in:
`src/main/resources/static/assets/postman-sql_commands/beerdb.sql`
### 🔐 Authentication
```http
POST /authenticate
{
  "email": "adam.mcloughlin@email.com",
  "password": "TempPass123"
}
```
Use the returned `access_token` for other API calls.
### 🔍 Sample Endpoints
```http
GET /api/customers/2/summary
POST /api/reviews
GET /api/breweries/1/report
GET /api/analytics/report
GET /api/analytics/qr-code
```
---
## 📁 Folder Structure
```bash
Assignment_One_Starter/
├── src/
│   ├── main/
│   │   ├── java/src/application/...
│   │   └── resources/
│   │       └── static/assets/postman-sql_commands/beerdb.sql
├── pom.xml
```
---
## 👨‍💻 Author
Adam McLoughlin  
Final Year IT Student – Technological University of the Shannon
---
## 📌 Disclaimer
This project is for academic use only. Any sensitive API tokens have been removed. The GitHub ZIP is intended for safe demonstration.
