# FocusFlow — Personal Productivity & Task Management Web Application

A full-featured personal productivity web application built with **Python**, **Flask**, and **SQLite**, designed to help users organize daily workflows, track completion streaks, analyze weekly productivity, and manage habits.

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.x-000000?style=flat&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=flat&logo=sqlite&logoColor=white)](https://sqlite.org/)

---

## 🌟 Core Features

- **User Authentication & Session Security**: Secure user registration, credential verification via Werkzeug password hashing (`generate_password_hash` / `check_password_hash`), and persistent sessions via Flask-Login.
- **Dynamic Task Management**:
  - Add tasks with priority and due dates (`POST /add`).
  - Toggle completion status with dynamic streak calculations (`GET /toggle/<id>`).
  - Safe task deletion (`GET /delete/<id>`).
- **Productivity Analytics & History**:
  - **Completion History** (`/history`): Review past completed tasks filtered by timeline.
  - **Weekly Overview** (`/weekly`): Visual breakdown of productivity performance across the 7-day calendar.
- **User Profile & Customization**:
  - Update display name and change password securely (`/profile`).
  - Dark/Light appearance theme configuration (`/settings`).
- **Data Portability**: Export complete task history directly to CSV format (`GET /export`).
- **Production Ready**: Includes Gunicorn `Procfile` for containerized or PaaS cloud hosting.

---

## 🛠️ Tech Stack

- **Backend**: Python 3, Flask, Flask-Login, Werkzeug Security
- **Database**: SQLite3 (`tasks.db`)
- **Frontend**: Jinja2 Templates, HTML5, CSS3, JavaScript
- **Server Deployment**: Gunicorn WSGI (`web: gunicorn app:app`)

---

## 📁 Repository Structure

```text
focusflow/
├── templates/
│   ├── index.html       # Primary task dashboard and active items
│   ├── login.html       # Authentication sign-in form
│   ├── register.html    # User registration form
│   ├── history.html     # Historical completion log
│   ├── weekly.html      # Weekly productivity breakdown
│   ├── profile.html     # User profile and password settings
│   └── settings.html    # Appearance and preference settings
├── .gitignore           # Excludes virtual environments and Python caches
├── app.py               # Application entrypoint, route handlers, and DB schema
├── Procfile             # Process definition for Gunicorn deployment
├── requirements.txt     # Python runtime dependencies
└── tasks.db             # SQLite database storing users and task records
```

---

## 🚀 Getting Started Locally

### Prerequisites
- Python 3.8 or newer
- pip package manager

### 1. Clone the Repository
```bash
git clone https://github.com/sujitha611/focusflow.git
cd focusflow
```

### 2. Set Up a Virtual Environment
```bash
python -m venv venv

# On Windows:
.\venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Application
```bash
python app.py
```

The web dashboard will be available at **`http://localhost:5000`**.

---

## 🧪 Testing & Verification Status

- **Syntax & Compilation**: Verified with `py_compile` (0 syntax errors).
- **Automated Test Suite**: No automated test suite present in this repository.

---

## 👤 Author
**Battu Jaya Sujitha**  
[GitHub Profile](https://github.com/sujitha611) | [LinkedIn](https://www.linkedin.com/in/jaya-sujitha-576b7a290/)
