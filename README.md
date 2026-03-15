# 🔐 Flask Authentication System

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Flask](https://img.shields.io/badge/Flask-Web_Framework-black)
![Database](https://img.shields.io/badge/Database-SQLite-green)
![Security](https://img.shields.io/badge/Security-Password_Hashing-orange)

A secure user authentication system built using **Flask**, **SQLAlchemy**, and **Flask-Login**.
This project demonstrates how to implement **secure login, password hashing, protected routes, and session management** in a Flask web application.

---

# 🚀 Features

* User Registration
* Secure Password Hashing (`pbkdf2:sha256`)
* User Login & Logout
* Session Management with **Flask-Login**
* Protected Routes using `@login_required`
* Secure File Download
* SQLite Database Integration
* Flash Messages for Authentication Feedback

---

# 🛠 Tech Stack

| Technology        | Purpose                             |
| ----------------- | ----------------------------------- |
| Python            | Programming Language                |
| Flask             | Web Framework                       |
| Flask-Login       | Authentication & Session Management |
| Flask-SQLAlchemy  | Database ORM                        |
| SQLite            | Lightweight Database                |
| Werkzeug Security | Password Hashing                    |
| Jinja2            | Template Engine                     |

---

# 📂 Project Structure

```
Flask-Authentication/
│
├── app.py
├── users.db
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   └── secrets.html
│
├── static/
│   └── files/
│       └── cheat_sheet.pdf
│
└── README.md
```

---

# ⚙️ Installation

Clone the repository

```
git clone https://github.com/ap-00007/Auth-with-Flask.git
cd flask-authentication-system
```

Create a virtual environment

```
python -m venv venv
```

Activate it

Mac / Linux

```
source venv/bin/activate
```

Windows

```
venv\Scripts\activate
```

Install dependencies

```
pip install flask flask_sqlalchemy flask_login werkzeug
```

---

# ▶️ Run the Application

Start the server:

```
python app.py
```

Open your browser:

```
http://127.0.0.1:5000
```

---

# 🔑 Authentication Flow

1. User registers with **email, name, and password**
2. Password is **hashed and salted** using `pbkdf2:sha256`
3. User is automatically logged in after registration
4. Flask-Login manages user sessions
5. Protected routes require authentication
6. Authenticated users can download protected resources

---

# 🔒 Security Implemented

* Password hashing with **salt**
* Secure password verification with `check_password_hash`
* Unique email constraint
* Session based authentication
* Protected routes
* Safe file serving

---

# 📌 Available Routes

| Route       | Description             |
| ----------- | ----------------------- |
| `/`         | Home page               |
| `/register` | Register new user       |
| `/login`    | Login page              |
| `/logout`   | Logout user             |
| `/secrets`  | Protected page          |
| `/download` | Download protected file |

---



# 📈 Possible Improvements

* Email verification
* Password reset functionality
* OAuth login (Google / GitHub)
* Rate limiting for login attempts
* CSRF protection
* Docker deployment
* PostgreSQL database support

---

# 👨‍💻 Author

Ashish Panda

---

