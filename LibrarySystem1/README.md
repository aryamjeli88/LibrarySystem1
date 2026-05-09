# 📚 YIC Library System

**Course:** CS381 — Web Application Development  
**College:** Yanbu Industrial College  

---

## 🚀 Setup Instructions

1. **Copy folder** to your server root:
   - Laragon: `C:\laragon\www\LibrarySystem\`
   - XAMPP:   `C:\xampp\htdocs\LibrarySystem\`

2. **Import database:**
   - Open `http://localhost/phpmyadmin`
   - Click **Import** → select `sql/library_db.sql` → click **Go**

3. **Open in browser:**
   - `http://localhost/LibrarySystem/`

---

## 🔑 Login Credentials

| Role    | Email              | Password    |
|---------|--------------------|-------------|
| Admin   | admin@yic.edu.sa   | password123 |
| Student | danah@gmail.com    | password123 |
| Student | lamar@gmail.com    | password123 |
| Student | refal@gmail.com    | password123 |

---

## ✅ Features

**Student:** Register · Login/Logout · Browse books · Search · Borrow · View history · Return books

**Admin:** Login/Logout · Dashboard with stats · View recent transactions · Manage books · Delete books

---

## 🔒 Security

- PDO Prepared Statements (SQL injection prevention)
- `htmlspecialchars()` on all output (XSS prevention)
- CSRF tokens on all POST forms
- `session_regenerate_id()` on login
- Server-side + client-side input validation
- Role-based access control
- `password_hash()` / `password_verify()`

---

## 📁 File Structure

```
LibrarySystem/
├── index.php
├── includes/
│   ├── config.php
│   └── csrf_helper.php
├── auth/
│   ├── login.php
│   ├── register.php
│   └── logout.php
├── student/
│   ├── browse.php
│   └── history.php
├── admin/
│   ├── dashboard.php
│   ├── manage_books.php
│   └── delete_book.php
├── actions/
│   ├── borrow.php
│   └── return.php
├── assets/
│   ├── css/style.css
│   └── js/script.js
└── sql/
    └── library_db.sql
```
