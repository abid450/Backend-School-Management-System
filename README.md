📌 School Management System – Features & Modules
school_management_system/


📁 School Management System – Project Structure Diagram

├── manage.py
│

├── school_management_system/

│   ├── __init__.py

│   ├── asgi.py

│   ├── wsgi.py

│   ├── urls.py

│   └── settings.py
│
├── apps/

│   │
│   ├── accounts/

│   │   ├── __init__.py

│   │   ├── admin.py

│   │   ├── apps.py

│   │   ├── models.py

│   │   ├── serializers.py

│   │   ├── views.py

│   │   ├── urls.py

│   │   └── signals.py
│   │
│   ├── students/

│   │   ├── admin.py

│   │   ├── models.py

│   │   ├── serializers.py

│   │   ├── views.py

│   │   └── urls.py
│   │
│   ├── attendance/

│   │   ├── admin.py

│   │   ├── models.py

│   │   ├── serializers.py

│   │   ├── views.py

│   │   ├── signals.py

│   │   └── urls.py
│   │
│   ├── academics/

│   │   ├── subjects.py

│   │   ├── exams.py

│   │   ├── results.py

│   │   ├── serializers.py

│   │   └── views.py
│   │
│   ├── reports/

│   │   ├── monthly_attendance.py

│   │   ├── summary.py

│   │   ├── ranking.py

│   │   └── views.py
│   │
│   └── notifications/

│       ├── email_service.py

│       ├── templates/

│       │   └── low_attendance.html

│       └── signals.py
│

├── templates/

│   └── emails/

│       └── attendance_warning.html

│
├── static/

│   ├── css/

│   ├── js/

│   └── images/
│

├── requirements.txt

├── .env

├── .gitignore

└── README.md



🎓 Student Management

• Student profile management (Name, Roll, Class, Section, Status)

• Active / Inactive student handling

• Advanced student search by name and roll

• Optimized queryset using select_related and prefetch_related


📚 Academic & Result Management

• Subject management

• Exam management (Mid Term, Test Exam, Final Exam)

• Student-wise subject marks entry

• Automatic total marks calculation

• Automatic average marks calculation

• Grade calculation based on percentage

• Student ranking system using Django Window Functions

• Exam-wise and subject-wise filtering support


🧮 Result Analytics

• Total marks aggregation

• Average marks aggregation

• Rank generation using DenseRank

• Class-wise performance analysis

• Student-wise performance analysis


🕒 Attendance Management

• Daily attendance tracking

• Attendance status support (Present / Absent / Late)

• One attendance per student per day restriction

• Attendance remarks support

• Automatic attendance summary generation


📊 Attendance Summary & Ranking

• Total attendance days calculation

• Present days count

• Absent days count

• Late days count

• Attendance-based ranking system

• Real-time updates using Django signals


📆 Monthly Attendance Report

• Automatic monthly attendance report generation

• Month-wise attendance statistics

• Present, absent, and late day calculation

• Attendance percentage calculation

• Class-wise filtering

• Section-wise filtering

• Student-wise filtering

• Optimized queries using TruncMonth


📈 Total Attendance Analytics

• Total present months calculation

• Total present days across all months

• Total class days calculation

• Overall attendance percentage calculation

• Ranking based on long-term attendance performance


🔔 Low Attendance Alert System

• Automatic low attendance detection

• Configurable attendance percentage threshold

• Automatic email alert sent to students

• Professional attendance warning messages

• Triggered automatically using Django signals


🔐 Authentication & Security

• JWT-based authentication (Access & Refresh token)

• Secure signup and login system

• Email verification support

• Password reset via email

• Device-based login tracking

• IP history tracking

• Device logout and block functionality

🛠 Admin Panel (Jazzmin UI)

• Modern and responsive admin dashboard

• Attendance summary view in admin panel

• Monthly attendance reports in admin

• Student attendance ranking overview

• Advanced search and filtering options


⚙️ Backend Architecture & Best Practices

• Django REST Framework (DRF)

• Clean service-layer architecture

• Signal-based automation

• Pagination for large datasets

• Optimized database queries

• Scalable and maintainable project structure


🌐 API Features

• RESTful API architecture

• Pagination support

• Search functionality

• Filtering support

• Secure API access using JWT

• Frontend and mobile app ready APIs


🚀 Technology Stack

• Backend: Django, Django REST Framework

• Authentication: JWT (SimpleJWT)

• Database: SQLite (upgradeable to PostgreSQL / MySQL)

• Admin UI: Jazzmin

• Email Service: SMTP (Gmail)

• Architecture: API-first design


🔮 Future Improvements

• Teacher management module

• Parent portal system

• Push notification system

• Attendance analytics charts
• Mobile application integration
• Role-based access control (Admin / Teacher / Student)


🛠 Project Tech Stack
Backend

* Python 3.10+

* Django 5.x

* Django REST Framework (DRF)

* Authentication & Security

* JWT Authentication (SimpleJWT)

* Email verification

* Password reset via email

* Database

* SQLite (Development)

* PostgreSQL / MySQL (Production ready)

* Admin Panel

* Django Admin

* Jazzmin (Modern UI)

* Email & Notification

* SMTP (Gmail)

* Automated low attendance alert system

* Tools & Utilities

* Git & GitHub

* Postman (API testing)

VS Code

⚙️ Installation Process

1️⃣ Clone the Repository
git clone https://github.com/your-username/school-management-system.git
cd school-management-system

2️⃣ Create Virtual Environment
python -m venv venv


Activate virtual environment:

Windows

venv\Scripts\activate


Linux / Mac

source venv/bin/activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Environment Variables Setup

Create a .env file in the root directory and add:

SECRET_KEY=your_secret_key
DEBUG=True

EMAIL_HOST=smtp.gmail.com

EMAIL_PORT=587

EMAIL_USE_TLS=True

EMAIL_HOST_USER=your_email@gmail.com

EMAIL_HOST_PASSWORD=your_app_password

5️⃣ Database Migration

python manage.py makemigrations
python manage.py migrate

6️⃣ Create Superuser
python manage.py createsuperuser

7️⃣ Run the Development Server
python manage.py runserver

🌐 Access the Application

Backend API: http://127.0.0.1:8000/

Admin Panel: http://127.0.0.1:8000/admin/

API Documentation (if enabled): http://127.0.0.1:8000/api/

🔑 Authentication Flow (JWT)

Login API returns Access Token & Refresh Token

Access Token used for secure API requests

Refresh Token used to regenerate Access Token

📦 API Ready for

Web Frontend

Mobile Application

Third-party integration

🚀 Deployment Ready

Environment-based settings

Secure secret key handling

Production database support

Scalable architecture

📌 Notes

Email alert system works automatically via Django signals

Attendance percentage threshold is configurable

Project follows clean and scalable architecture

