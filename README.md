# 📚 BookBazaar: Library Management & Review System

## 📖 Project Overview
**BookBazaar** is a full-stack library management system integrating **SQLite** and **MongoDB** for book storage and user reviews. It provides **book and author management, inventory tracking, user reviews, API development with Flask, testing via Postman, and deployment using Apache on Windows**.

---

## 🚀 Features
- 📖 **Book & Author Management** – CRUD operations.
- 🏷️ **Inventory & Sales Tracking** – Manage stock and transactions.
- ⭐ **User Reviews** – Store and retrieve reviews via MongoDB.
- 🌍 **RESTful APIs** – Secure API endpoints.
- 🗄️ **Hybrid Database Integration** – SQLite (structured data) + MongoDB (reviews).
- 🔗 **Postman Testing** – API validation.
- 🌐 **Apache Deployment (Windows)** – Production-ready setup.

---

## 🏗️ Project Structure

```
📂 BookBazaar/
├── 📂 apache_config/       # Apache configuration files (httpd.conf, httpd-vhosts.conf)
├── 📂 api/                 # Flask API logic
│   ├── 📂 routes/          # API endpoints
│   ├── 📂 services/        # Business logic & database interactions
├── 📂 app/                 # Core application
│   ├── 📂 models/          # Database models
│   ├── 📂 database/        # SQLite & MongoDB collections
├── 📂 config/              # Configuration files
├── 📂 documentation/       # API documentation
├── 📂 postman/             # Postman collection for API testing
├── 📜 requirements.txt     # Dependencies
├── 📜 run.py               # App entry point
├── 📜 wsgi.py              # WSGI for Apache deployment
└── 📜 README.md            # Documentation
```

---

## 🔧 Setup & Installation (Windows)

### 1️⃣ **Run the Application**
1. **Clone the repository:**
   ```sh
   git clone https://github.com/MohamedFarrag28/BookBazaar-Library-Management.git
   cd BookBazaar-Library-Management
   ```

2. **Run the startup script:**
   ```sh
   python run.py
   ```

   This will:
   - Set up SQLite database.
   - Start the MongoDB service (if not running).
   - Launch the Flask API.

---

## 🌐 API Endpoints

| Method | Endpoint                  | Description                |
|--------|---------------------------|----------------------------|
| GET    | `/books`                   | Fetch all books            |
| POST   | `/books`                   | Add a new book             |
| GET    | `/books/<id>`               | Retrieve book details      |
| PUT    | `/books/<id>`               | Update book details        |
| DELETE | `/books/<id>`               | Remove a book              |
| GET    | `/books/<id>/reviews`       | Fetch book reviews         |
| POST   | `/books/<id>/reviews`       | Add a review for a book    |
| PUT    | `/reviews/<review_id>`      | Update a review            |
| DELETE | `/reviews/<review_id>`      | Delete a review            |

Full API details are available in [`documentation/API.md`](documentation/API.md).

---

## 🏗️ Deployment on Windows (Apache & mod_wsgi)

### **Steps to Deploy**
1. **Configure Apache**
   - Modify the configuration files in `apache_config/`:
     - **`httpd.conf`**: Load the WSGI module and include `httpd-vhosts.conf`.
     - **`httpd-vhosts.conf`**: Define virtual hosts for the API.

2. **Restart Apache**
   ```sh
   httpd.exe -k restart
   ```

3. **Access the App**
   ```
   http://localhost/
   ```

---

## 🧪 Testing with Postman
1. Import the **Postman collection** from `postman/BookBazaar.postman_collection.json`.
2. Test **CRUD operations** on books and reviews.
3. Verify **error handling**.

---

## 📜 Documentation
- 📄 **Project Overview** – Features and setup.
- 🗃️ **Database Schema** – ER diagrams & structure.
- 🔍 **API Reference** – Endpoints and responses.
- 🏗️ **Deployment Guide** – Local & server setup.
- 🚀 **Troubleshooting** – Common issues and fixes.

Full documentation is available in [`documentation/`](documentation/).

---

🚀 **Happy Coding!**
