# 🟩 FRONTEND — HTML + JavaScript

## 📌 Overview

The frontend is a **simple static UI** built using:

* HTML
* CSS
* JavaScript (jQuery)

It communicates with the backend directly using AJAX.

---

## 🚀 Running Frontend

The frontend should NOT be placed inside Spring Boot.

Instead, place the frontend folder anywhere and open the pages using Live Server.

### Option 1 — VS Code Live Server (Recommended)

Right-click `index.html` → **Open with Live Server**

URL will be:

```
http://127.0.0.1:5500/index.html
```

---

## 🔧 Update API Base URL

In frontend files, update the backend URL:

```
const BASE_URL = "http://localhost:8080";
```

---

## 🔐 Authentication Flow in Frontend

1. User logs in → token stored in localStorage.
2. Every API call sends:

```
headers: { Authorization: "Bearer " + token }
```

---

## 📌 Pages

### 🔹 `login.html`

* User login
* Stores JWT token

### 🔹 `index.html`

* Displays student list
* Shows images from backend

### 🔹 `create-edit.html`

* Create or update student
* Upload photo
* Dynamically add/remove subjects

---

## 📁 Folder Structure

```
frontend/
│── index.html
│── login.html
│── create-edit.html
```

---

## ⚠️ CORS Requirement

Backend must allow:

```
http://127.0.0.1:5500
```

Otherwise AJAX requests will fail.

---

## 🧪 Testing the App

1. Start backend → `http://localhost:8080`
2. Start frontend (Live Server) → `http://127.0.0.1:5500`
3. Login
4. Create students
5. View students on index page

---