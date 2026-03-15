# Flask Authentication System 🔐

A simple authentication system built with Flask that allows users to register, log in, securely store passwords, and download protected files.
This project demonstrates secure authentication practices using Flask, SQLAlchemy, and Flask-Login.

---

## Features

* User registration
* Secure password hashing with `pbkdf2:sha256`
* Login and logout functionality
* Session management using Flask-Login
* Protected routes accessible only to authenticated users
* Secure file download for logged-in users
* SQLite database for storing user data

---

## Tech Stack

* Python
* Flask
* Flask-Login
* Flask-SQLAlchemy
* SQLite
* Werkzeug Security
* Jinja2 Templates

---

## Project Structure

```
project/
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

## Installation

Clone the repository

```bash
git clone https://github.com/ap-00007/Auth-with-Flask.git
cd flask-authentication-system
```

Create a virtual environment

```bash
python -m venv venv
```

Activate the environment

Mac/Linux:

```bash
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

Install dependencies

```bash
pip install flask flask_sqlalchemy flask_login werkzeug
```

---

## Running the Application

Start the Flask server:

```bash
python app.py
```

Open your browser and go to:

```
http://127.0.0.1:5000
```

---

## Authentication Flow

1. User registers with email, name, and password.
2. Password is hashed and salted using `pbkdf2:sha256`.
3. User is automatically logged in after registration.
4. Protected routes (`/secrets` and `/download`) require authentication.
5. Flask-Login manages user sessions.
6. Logged-in users can download protected files.

---

## Security Features

* Password hashing with salt
* Unique email constraint in database
* Session-based authentication
* Protected routes using `@login_required`
* Secure file serving using `send_from_directory()`

---

## Example Routes

| Route       | Description             |
| ----------- | ----------------------- |
| `/`         | Home page               |
| `/register` | User registration       |
| `/login`    | User login              |
| `/logout`   | Log out current user    |
| `/secrets`  | Protected page          |
| `/download` | Download protected file |

---

## Future Improvements

* Email verification
* Password reset functionality
* OAuth login (Google/GitHub)
* User profile dashboard
* Better UI styling

---

## Author

Ashish Panda

---

## License

This project is for educational purposes.
