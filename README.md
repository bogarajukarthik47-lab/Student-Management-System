Cloud-Based Student Management System

A role-based, web app for Student Management, built using Python FastAPI, SQLAlchemy, and Jinja2 templates. Manages students, professors, admins, assignments, attendance, grades, and file uploads.

About the Project:

This application provides web-based dashboards for Admins, Professors, and Students, supporting secure authentication, CRUD operations, data export, and assignment/file handling. It's designed for fast local deployment and User friendly.


Features:

Role-based authentication and authorization

Separate dashboards for Admin, Professor, Student

Add/update/delete users (Admin, Professor, Student)

Assignment and submission workflows (Professor and Student)

Marks and attendance management (Professor)

File upload/download (Assignments, submissions)

CSV export of marks and attendance for authorized roles

Secure password hashing with Passlib

HTML rendering with Jinja2 templates

Data persistence with SQLAlchemy ORM. It involves mapping Python classes to database tables and managing the state of objects in a database using the Object Relational Mapper (ORM).



Technologies Used:

Python FastAPI -- For Application Backend
Passlib        -- For Password Hashing
Jinja          -- For Web Templates
PostgreSQL     -- Database
HTML,CSS       -- Web Frontend
Docker         -- Containerization
Uvicorn        -- For running the application



Project Structure:

SMS/
├── app/
│   ├── __init.py__
│   ├── auth.py
│   ├── database.py
│   ├── main.py
│   ├── models.py
│   ├── schemas.py
│   ├── utils.py
│   ├── static/
│   ├── templates/
│   │   ├── add_admin.html
│   │   ├── add_assignment.html
│   │   ├── add_attendance.html
│   │   ├── add_marks.html
│   │   ├── add_professor.html
│   │   ├── add_student.html
│   │   ├── admin_dashboard.html
│   │   ├── dashboard.html
│   │   ├── login.html
│   │   ├── professor_dashboard.html
│   │   ├── professor_upload.html
│   │   ├── student_dashboard.html
│   │   ├── submit_assignment.html
│   ├── uploads/
├── Dockerfile
├── .dockerignore
├── requirements.txt



Prerequisites:

Python 3.8+

PostgreSQL server running locally and accessible

pip for Python packages

Docker (for containerized deployment)

Uvicorn (recommended for running application)


Installation:

1. Clone the repo

   git clone <repo URL>

2. Install Dependencies

   python
   pip  
   pip install -r requirements.txt

3. Configure PostgreSQL locally and pass the connection string in app/database.py file. Create PostgreSQL DB after the setup. (eg:"postgresql://postgres:postgres@localhost:5432/studentdb")

4. Set up initial users

   Defaults: Admin, Professor, Student are auto-created at first run.


Usage:

Run with Uvicorn

   python -m uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

   visit https://localhost:8000/login for the login page


Sample Credentials:

Role          UserName         Password

Admin         admin            admin123
Professor     prof1            prof123
Student       student1         stud123





