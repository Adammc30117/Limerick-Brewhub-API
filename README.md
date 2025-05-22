# Limerick Brewhub API

A Spring Boot backend application for managing and analyzing craft beer reviews, breweries, and customer engagement across the EMEA region. Developed as part of an API Design & Development module.

---
## 🚀 Features
* **Task 1**: Customer summaries and brewery PDF reports with JSON, XML, TSV responses
* **Task 2**: Add/update reviews, prevent duplicates, auto-update average ratings
* **Task 3**: Generate analytics report + QR code linking to GitHub-hosted PDF
---
## 📦 Tech Stack
* Java 17, Spring Boot
* Spring Data JPA & MySQL
* JWT Authentication
* Apache PDFBox, ZXing, JFreeChart
---
## 🔐 Authentication
**Login:**
```http
POST /authenticate
{
  "email": "adam.mcloughlin@email.com",
  "password": "TempPass123"
}
```
Use the returned `access_token` in the `Authorization` header.
---
## 📬 Sample Endpoints
```http
GET /api/customers/2/summary
POST /api/reviews
GET /api/breweries/1/report
GET /api/analytics/report
GET /api/analytics/qr-code
```
---
## 🗃 SQL Commands
Located in: `static/assets/sql/beerdb.sql`

Includes:
* Check average ratings
* Fetch reviews by user/beer
* List breweries with reviews
---
## 🛠 How to Run
```bash
1. Set up MySQL DB (e.g., beeranalytics)
2. Configure application.properties
3. Run:
   mvn clean install
   mvn spring-boot:run
```
---
## 📁 Folder Structure
```bash
Assignment_One_Starter/
├── src/
│   ├── main/
│   │   ├── java/src/application/...
│   │   └── resources/
│   │       └── static/assets/sql/beerdb.sql
├── pom.xml
```
---
## 👨‍🎓 Author
Adam McLoughlin  
Final Year IT Student  
Technological University of the Shannon
---
## 📌 Disclaimer
This project is for academic purposes only. Any real tokens have been removed. The zipped project is provided for grading and demonstration purposes only.
