# 🚀 API Testing - Restful Booker (Postman & Newman)

This repository contains an automated API testing suite for the **Restful Booker** platform. It demonstrates complete CRUD operations, dynamic data sharing between requests, and data-driven testing strategies.

---

## 📊 Project Structure & Data-Driven Testing

The collection covers all main endpoints (`/auth`, `/booking`) using dynamic environment variables to pass data (like Tokens and IDs) from one request to the next.

💡 **Data-Driven Testing (CSV Integration):**
To test boundary values and bulk operations, this project utilizes the included **CSV data file**. Postman and Newman dynamically inject these rows into the payloads to run multiple test scenarios automatically.

---

## 🧪 Automated Assertions

Every request includes JavaScript assertions to validate:

- **Status Codes** (`200 OK`, `201 Created`, `404 Not Found`, etc.)
- **Response Time** (Ensuring performance benchmarks under 500ms)
- **JSON Schema** (Verifying data integrity and correct data types)

---

## 🚀 How to Run the Tests

### Option 1: Via Postman GUI

1. Import `Collection.json` and `Environment.json` into Postman.
2. Open **Collection Runner**, select the **CSV file** as your data source, and execute.

### Option 2: Via Linux Terminal (Newman)

To run the full suite along with your CSV data file headlessly, execute:

```bash
newman run Collection.json -e Environment.json -d tvoj_fajl.csv
```
