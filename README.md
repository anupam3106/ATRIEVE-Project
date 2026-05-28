# ATRIEVE-Project
ATRIEVE is a full-featured Lost and Found platform built with Django (Python) and SQLite. It supports user authentication (including Google OAuth), lost/found item reporting, staff-moderated claim requests, automatic item matching, in-app notifications, and a responsive dark/light theme UI.
# 🔍 ATRIEVE – Smart Lost and Found System

> *Reuniting people with their lost belongings — quickly, securely, and with the power of community.*

![Python](https://img.shields.io/badge/Python-3.12+-blue?style=flat&logo=python)
![Django](https://img.shields.io/badge/Django-4.x-green?style=flat&logo=django)
![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey?style=flat&logo=sqlite)
![License](https://img.shields.io/badge/License-Academic-orange?style=flat)

---

## 📌 About

**ATRIEVE** (a portmanteau of *retrieve*) is a web-based Lost and Found Management System developed as a final year project for the **Bachelor of Computer Applications (BCA)** programme at L. N. Mishra College of Business Management, B.R.A. Bihar University, Muzaffarpur.

The system provides a centralized digital platform where users can report lost items, report found items, browse listings, submit claim requests, and receive real-time notifications — all with a staff-moderated workflow to prevent fraud.

---

## ✨ Features

- 🔐 **User Authentication** — Register, login (username/email), logout, Google OAuth via django-allauth
- 📦 **Lost & Found Reporting** — Report items with name, category, description, location, date, and image
- 🔎 **Smart Search & Filter** — Search by name, filter by category and location
- 🤝 **Claim Request Workflow** — Submit claims with proof of ownership; staff approves/rejects
- 🔔 **Notification System** — In-app notifications for item matches, claim updates, and admin alerts
- 🤖 **Auto-Matching** — Automatically matches found items with existing lost reports
- ⏱️ **Auto-Expiry** — Items auto-deactivate 12 hours after claim approval
- 👥 **Role-Based Access** — Regular users, Staff, and Admin roles
- 🌙 **Dark / Light Theme** — User preference saved in profile
- 📋 **Activity Log** — All staff actions are logged for accountability

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Django 4.x (Python 3.12+) |
| Frontend | HTML5, CSS3, JavaScript (ES6+) |
| Database | SQLite (development) |
| Authentication | Django Auth + django-allauth (Google OAuth) |
| Version Control | Git |
| Package Manager | pip |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.12+
- pip
- Git

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/ATRIEVE-Project.git
cd ATRIEVE-Project

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate        # Linux/Mac
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Apply migrations
python manage.py migrate

# 5. Create superuser (admin)
python manage.py createsuperuser

# 6. Run the development server
python manage.py runserver
```

Then open `http://127.0.0.1:8000` in your browser.

---

## 📁 Project Structure

```
ATRIEVE-Project/
├── AtrieveLostFound/          # Main Django project settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── lostfound/                 # Core application
│   ├── models.py              # Database models
│   ├── views.py               # View functions & business logic
│   ├── forms.py               # Django form classes
│   ├── urls.py                # URL routing
│   ├── admin.py               # Admin panel config
│   ├── templates/             # HTML templates
│   ├── static/                # CSS & JavaScript files
│   └── management/
│       └── commands/
│           └── expire_claimed_items.py
├── media/                     # Uploaded images
├── static/                    # Global static files
└── manage.py
```

---

## 👤 User Roles

| Role | Permissions |
|------|------------|
| **User** | Register, report items, submit claims, view notifications |
| **Staff** | All user permissions + review & approve/reject claims |
| **Admin** | Full access via Django admin panel + staff dashboard |

---

## 📸 Screenshots

| Home Page | Dashboard | Claim Status |
|-----------|-----------|--------------|
| ![Home](download/home.png) | 

---

## ⚙️ Management Commands

```bash
# Expire claimed items older than 12 hours (run via cron in production)
python manage.py expire_claimed_items
```

---

## 🔮 Future Scope

- 📧 Email & SMS notifications (SMTP / Twilio)
- ⚡ Real-time updates via Django Channels & WebSockets
- 🤖 ML-based item matching (NLP / image recognition)
- 📱 Mobile app (React Native / Flutter)
- 🗺️ Geolocation support (Leaflet.js / Google Maps)
- 🗄️ PostgreSQL migration for production
- 🌐 Multi-language support (Hindi + regional languages)

---

## 👩‍💻 Developer

**Anupam Kumari**
- Roll No: 235220
- BCA Final Year — Session 2023–2026
- L. N. Mishra College of Business Management, Muzaffarpur
- B.R. Ambedkar Bihar University, Muzaffarpur

---

## 🙏 Acknowledgements

Special thanks to:
- **Shri Anil Kumar** — Project Guide
- **Surendra Sir & Pradeep Sir** — Technical Mentorship
- **Miss Anjali Kumari** — UI/UX Design Suggestions

---

## 📄 License

This project is submitted for academic purposes under the BCA programme of B.R.A. Bihar University, Muzaffarpur (2023–2026).

---

*© 2026 Atrieve. Built for safe lost & found recovery.*
