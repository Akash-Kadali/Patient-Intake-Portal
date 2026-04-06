<p align="center">
  <a href="https://laravel.com" target="_blank">
    <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
  </a>
</p>

<h1 align="center">Patient Intake Portal</h1>

<p align="center">
  A role-based medical clinic management platform built with Laravel for handling appointments, patient workflows, doctor access, and administrative operations.
</p>

---

## Overview

Patient Intake Portal is a full-stack clinic workflow system designed to simplify day-to-day medical front-desk and doctor-side operations. It supports appointment scheduling, patient record handling, doctor-patient management, and controlled user administration through a role-based access model.

The system is designed to reduce manual intake overhead, organize patient data more clearly, and improve operational flow across clinic staff.

---

## Core Features

- Manage clinic workflows through secure role-based access
- Create and track appointments efficiently
- View and manage registered patients and doctors
- Maintain patient profiles and treatment-related records
- Control user access and permissions from an admin layer
- Support clinic staff with a structured and easy-to-use dashboard

---

## Role-Based Access

The platform includes three user roles, each with different permissions.

### Secretary
A secretary can:

- Log in securely
- Create new appointments
- View the list of registered patients
- View the list of registered doctors

### Doctor
A doctor can do everything a secretary can, and also:

- Manage patients assigned through appointments
- View and update patient-related information
- Access and manage patient profiles

### Admin
An admin can do everything a doctor and secretary can, and also:

- Manage application users
- Control access across the platform
- Oversee clinic-wide operations from the admin layer

---

## Use Case Diagram

![Use Case Diagram](./public/useCaseDiagram.png)

---

## Tech Stack

- **Laravel 9** — Backend framework and application architecture
- **PHP** — Server-side logic
- **MySQL** — Relational database
- **Blade** — Templating engine
- **AdminLTE** — Dashboard UI template
- **Bootstrap** — Frontend styling and layout
- **NPM** — Frontend dependency management
- **Composer** — PHP dependency management

---

## Why This Project

This project was built to model a real clinic intake and management workflow in a structured web application. Instead of handling appointments and patient information manually, the portal centralizes everything in one role-aware system.

It is especially useful for demonstrating:

- Full-stack Laravel development
- Role-based authorization
- CRUD-heavy workflow design
- Database-backed patient and appointment handling
- Practical healthcare-oriented software architecture

---

## Project Highlights

- Built a multi-role clinic management system with separate access levels for secretary, doctor, and admin users
- Structured appointment creation and patient assignment workflows for smoother clinic coordination
- Organized patient profile management around doctor-patient relationships
- Integrated admin-level user control for secure operational oversight
- Used Laravel conventions to keep the codebase modular, maintainable, and scalable

---

## Installation Guide

### 1. Clone the repository

```bash
git clone https://github.com/abdelghanyMh/laravel_medical.git
cd laravel_medical
````

### 2. Install dependencies

```bash
composer install
npm install
```

### 3. Configure environment

Copy the example environment file:

```bash
cp .env.example .env
```

Then update the database values inside `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=root
DB_PASSWORD=your_password
```

### 4. Generate application key

```bash
php artisan key:generate
```

### 5. Run database migrations

```bash
php artisan migrate
```

### 6. Seed the database (optional)

```bash
php artisan db:seed
```

> Check `database/seeders/DatabaseSeeder.php` for seeded records and default users.

### 7. Build frontend assets

```bash
npm run dev
```

### 8. Start the development server

```bash
php artisan serve
```

The app should now be available locally at:

```bash
http://127.0.0.1:8000
```

---

## Demo Login Credentials

If you seeded the database, the following demo users are available:

| Role      | Email                                                             | Password |
| --------- | ----------------------------------------------------------------- | -------- |
| Admin     | [admin@clinictlemcen.com](mailto:admin@clinictlemcen.com)         | 123456   |
| Doctor    | [doctor@clinictlemcen.com](mailto:doctor@clinictlemcen.com)       | 123456   |
| Doctor    | [doctor2@clinictlemcen.com](mailto:doctor2@clinictlemcen.com)     | 123456   |
| Secretary | [secretary@clinictlemcen.com](mailto:secretary@clinictlemcen.com) | 123456   |

---

## Folder Structure Snapshot

```bash
app/
bootstrap/
config/
database/
public/
resources/
routes/
storage/
tests/
```

Important areas:

* `app/Models` → Eloquent models
* `app/Http/Controllers` → Application controllers
* `resources/views` → Blade templates
* `routes/web.php` → Web routes
* `database/migrations` → Database schema
* `database/seeders` → Seed data

---

## Security and Access Design

This project uses role-aware access control so that users only interact with the parts of the system relevant to their responsibilities.

* Secretaries focus on appointment coordination
* Doctors focus on patient management
* Admins manage the entire platform and user access

This separation helps keep workflows clean, secure, and operationally realistic.

---

## Possible Future Improvements

* Add patient medical history timeline
* Add prescription management
* Add billing and invoice support
* Add appointment reminders by email or SMS
* Add search and filtering across patients and doctors
* Add analytics dashboard for appointments and clinic usage
* Add audit logs for admin-level actions
* Add REST API support for external integrations

---

## Screenshots

You can add your application screenshots here for better presentation.

Example sections:

* Login Page
* Dashboard
* Appointment Creation
* Patient List
* Doctor Panel
* Admin User Management

---

## What This Project Demonstrates

This project is a strong example of:

* Laravel-based full-stack development
* Real-world workflow mapping
* Clean separation of roles and permissions
* CRUD architecture in healthcare software
* Dashboard-driven business application design

It is suitable for showcasing backend engineering, web application development, and practical product thinking in portfolio, internship, or job applications.

---

## Acknowledgements

* [Laravel](https://laravel.com/)
* [AdminLTE](https://adminlte.io/themes/v3/)

---
