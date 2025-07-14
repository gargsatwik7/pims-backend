<<<<<<< HEAD
# pims-backend
=======

# 📊 Project Info Management System (PIMS) - Backend

This is the backend for the **Project Info Management System (PIMS)** built with **Django** and **Django REST Framework**. It allows authenticated users with different roles (Admin, Manager, Employee) to manage projects, clients, teams, members, and assignments efficiently.

---

## 🚀 Features

- ✅ User authentication (Login/Logout)
- ✅ Role-based permissions (Admin, Manager, Employee)
- ✅ Project & Client management
- ✅ Member assignment tracking
- ✅ Filter, search, and pagination in APIs
- ✅ Token-based authentication (DRF)
- ✅ Secure credentials handling

---

## 🔧 Tech Stack

- Python 3.x
- Django 4.x
- Django REST Framework
- MySQL / SQLite (default)
- JWT / Token Authentication (optional)

---

## 📁 Folder Structure

```
pims_backend/
├── core/               # Main app with models and views
├── pims_backend/       # Django settings & urls
├── manage.py           # Entry point
├── db.sqlite3          # Database (if using SQLite)
└── requirements.txt    # Dependencies
```

---

## 🔐 User Roles

| Role      | Permissions                                                                 |
|-----------|------------------------------------------------------------------------------|
| Admin     | Full control (CRUD on all models, manage users, roles)                      |
| Manager   | Can view, assign, and update projects and members                           |
| Employee  | Can view own assigned tasks and update limited fields (like status)         |

---

## 🛠️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/gargsatwik7/pims-backend.git
cd pims-backend
```

### 2. Create Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate  # On Windows
# OR
source venv/bin/activate  # On Mac/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Superuser

```bash
python manage.py createsuperuser
```

### 6. Start Server

```bash
python manage.py runserver
```

Go to: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

---

## 📡 API Overview

| Method | Endpoint                        | Description                |
|--------|----------------------------------|----------------------------|
| POST   | `/api/login/`                   | Login and receive token    |
| GET    | `/api/projects/`                | List all projects          |
| POST   | `/api/clients/`                 | Create a client (admin)    |
| GET    | `/api/members/assigned/`        | View assigned members      |
| POST   | `/api/logout/`                  | Logout user                |

👉 More endpoints available inside `core/views.py` or using tools like Postman.

---

## 🔒 Authentication

- Uses **TokenAuthentication** from DRF.
- Add token in headers:

```http
Authorization: Token your-token-here
```

---

## 📌 Future Improvements

- JWT support
- Export reports (PDF/CSV)
- Frontend integration (React)
- Real-time updates using Channels

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you’d like to change.

---

## 🧑‍💻 Developer

- **Name:** Satwik Garg
- **Email:** gargsatwik7@gmail.com
- **GitHub:** [gargsatwik7](https://github.com/gargsatwik7)

---

## 📜 License

This project is licensed under the MIT License.
>>>>>>> 76278bb6aab2f81280d8b2666e08466503cc22ec
