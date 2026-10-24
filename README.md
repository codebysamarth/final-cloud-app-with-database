# Online Course Application with Assessment Feature

A comprehensive Django-based e-learning platform with an integrated exam and assessment system, developed as the final project submission for the Coursera course **Django Application Development with SQL and Databases** (IBM).

---

## Project Overview

This project extends an existing `onlinecourse` Django web application by implementing a complete assessment/exam subsystem:
- **Assessment Models**: `Question`, `Choice`, and `Submission` models linked to courses, lessons, and student enrollments.
- **Admin Dashboard Integration**: Inline administration for managing questions and choices directly within courses and lessons via `QuestionInline`, `ChoiceInline`, `QuestionAdmin`, and `LessonAdmin`.
- **Exam Taking Interface**: Dynamic, responsive course exam views with Bootstrap collapsible components, multi-choice checkbox selection, and CSRF protection.
- **Result Calculation & Display**: Automated exam grading, pass/fail thresholds (passing score 80%), answer review highlighting correct vs. incorrect choices, and score reporting.

---

## ER Diagram

![Onlinecourse ER Diagram](static/media/course_images/onlinecourse_app_er.png)

---

## Project Architecture

```text
final-cloud-app-with-database/
├── manage.py
├── myproject/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── onlinecourse/
│   ├── models.py                  # Course, Lesson, Question, Choice, Submission models
│   ├── admin.py                   # Admin site integration with inlines
│   ├── views.py                   # Submit and show_exam_result views
│   ├── urls.py                    # URL routing for exam submission and results
│   └── templates/onlinecourse/
│       ├── course_detail_bootstrap.html     # Course detail and exam form
│       ├── course_details_bootstrap.html    # Course detail view
│       ├── exam_result_bootstrap.html       # Exam result and grading review
│       ├── course_list_bootstrap.html       # Course catalog
│       └── user_login_bootstrap.html        # Authentication
└── README.md
```

---

## Setup & Running Locally

1. **Clone the repository:**
   ```bash
   git clone <repository_url>
   cd final-cloud-app-with-database
   ```

2. **Install dependencies:**
   ```bash
   pip install django
   ```

3. **Apply database migrations:**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create a superuser:**
   ```bash
   python manage.py createsuperuser
   ```

5. **Run the development server:**
   ```bash
   python manage.py runserver
   ```
   Navigate to `http://localhost:8000` for the course application or `http://localhost:8000/admin` for the admin portal.

---

## Author

- **Course:** Django Application Development with SQL and Databases
- **Developer:** Samarth
