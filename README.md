# 📚 EduTrack — Education Management System

A full-stack web application for managing college education operations across three roles: **Student**, **Teacher**, and **Admin**.

Built as a final-year B.Tech project for a QSpiders internship presentation.

---

## 🚀 Features

### 🎓 Student
- View enrolled courses, attendance, and results
- Track assignment submissions and deadlines
- Check fee payment status
- Read notices posted by teachers/admin

### 👨‍🏫 Teacher
- Mark student attendance
- Upload results (internal + external)
- Post and grade assignments
- Post notices to students

### 🛠️ Admin
- Add/remove students and teachers
- Manage course and department data
- Update fee records
- Full oversight dashboard

---

## 🧰 Tech Stack

| Layer      | Technology          |
|------------|---------------------|
| Frontend   | React 19.2          |
| Backend    | Flask 2.3 (Python)  |
| Database   | MySQL               |
| ORM        | SQLAlchemy          |
| Auth       | bcrypt              |
| Runtime    | Python 3.12.10      |

---

## 📁 Project Structure

```
edutrack/
├── edutrack-main/           # Flask backend
│   ├── app.py               # Main application & API routes
│   ├── models.py            # SQLAlchemy ORM models
│   ├── populate.py          # Database seeding script
│   └── requirements.txt
│
└── edutrack-frontend-master/  # React frontend
    ├── src/
    │   ├── pages/           # Role-based dashboards
    │   │   ├── StudentDashboard.jsx
    │   │   ├── TeacherDashboard.jsx
    │   │   └── AdminDashboard.jsx
    │   ├── App.js
    │   └── index.js
    └── package.json
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.12.10
- Node.js & npm
- MySQL Server

### Backend

```bash
cd edutrack-main
pip install -r requirements.txt
python app.py
```

Make sure your MySQL server is running and the database is configured in `app.py`.

### Frontend

```bash
cd edutrack-frontend-master
npm install
npm start
```

The app will run at `http://localhost:3000` with the Flask backend at `http://localhost:5000`.

---

## 🗄️ Database

The system uses MySQL with SQLAlchemy ORM. Run the populate script to seed the database:

```bash
python populate.py
```

This generates:
- 400 students (distributed across 4 years)
- 60 teachers (across 5 departments)
- 3 admin accounts
- 20 courses, attendance records, results, assignments, and fee entries

### Test Credentials

| Role    | Email               | Password |
|---------|---------------------|----------|
| Student | student@test.com    | test123  |
| Teacher | teacher@test.com    | test123  |
| Admin   | admin@test.com      | test123  |

---

## 🔌 API Overview

| Method | Endpoint                    | Description               |
|--------|-----------------------------|---------------------------|
| POST   | `/api/login`                | Authenticate user         |
| GET    | `/api/student/dashboard`    | Student dashboard data    |
| GET    | `/api/teacher/dashboard`    | Teacher dashboard data    |
| GET    | `/api/admin/dashboard`      | Admin dashboard data      |
| POST   | `/api/attendance/mark`      | Mark attendance           |
| POST   | `/api/result/upload`        | Upload student result     |
| POST   | `/api/assignment/post`      | Post new assignment       |
| POST   | `/api/notice/post`          | Post notice               |
| POST   | `/api/admin/add-student`    | Add new student           |
| POST   | `/api/admin/add-teacher`    | Add new teacher           |
| DELETE | `/api/admin/delete-student` | Remove student            |
| DELETE | `/api/admin/delete-teacher` | Remove teacher            |
| PUT    | `/api/admin/update-fee`     | Update fee record         |

---

## 👤 Author

**Utkarsh Mishra**  
GitHub: [@Utkarsh7106](https://github.com/Utkarsh7106)

---

## 🤝 Acknowledgements

- **Shrishti Mishra** / [@shrishtimishra09](https://github.com/shrishtimishra09) — Frontend collaboration (early phase)
- QSpiders for the internship project framework

---

## 📄 License

This project is intended for academic purposes only.
