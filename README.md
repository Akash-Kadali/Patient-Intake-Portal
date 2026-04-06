<p align="center">
  <a href="https://laravel.com" target="_blank">
    <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
  </a>
</p>

<h1 align="center">Patient Intake Portal</h1>

<p align="center">
  A full-stack Laravel application for managing clinic intake, appointments, patient records, doctor workflows, and admin operations through a secure role-based system.
</p>

<p align="center">
  Built to model a practical medical front-desk and doctor-side workflow with clean access control, maintainable backend structure, and production-style organization.
</p>

---

## About the Project

Patient Intake Portal is a role-based clinic management system built using Laravel. I designed this project to simulate how a real medical clinic handles patient intake, appointment booking, doctor assignment, and administrative control inside a single web platform.

Instead of treating it like a simple CRUD app, I structured it as an operational workflow system where each role has clear boundaries and responsibilities. The main goal was to make day-to-day clinic actions easier to manage, reduce manual coordination, and keep the system organized through controlled access.

This project reflects the kind of software I like building: practical systems, clear backend structure, and applications that solve real workflow problems instead of just displaying forms and tables.

---

## What the System Does

- Handles patient intake and clinic appointment workflows
- Supports secure login with role-based access
- Allows staff to create and manage appointments
- Helps doctors manage patients assigned through appointments
- Maintains patient profile information inside the system
- Gives admins full control over user management and platform access
- Keeps clinic operations organized through separated responsibilities

---

## Role-Based Access Model

The application includes three user roles.

### Secretary

A secretary can:

- Log in to the system
- Create new appointments
- View registered patients
- View registered doctors

### Doctor

A doctor can do everything a secretary can, and also:

- Manage patients assigned through appointments
- Access and update patient-related details
- Manage patient profiles linked to their care flow

### Admin

An admin can do everything a doctor and secretary can, and also:

- Manage all platform users
- Control system-level access
- Oversee clinic-wide operations

This separation makes the system more realistic, more secure, and easier to manage.

---

## Why I Built This

I built this project to explore how healthcare workflow software can be structured in a clean and maintainable way using Laravel. I wanted to build something beyond a generic dashboard project, so I focused on a use case with clear actors, real constraints, and meaningful access control.

The interesting part of this system is not only storing records, but organizing how different users interact with the same clinic workflow in different ways. That design thinking is what makes the project stronger.

This project helped me work more deeply on:

- Laravel application structure
- Authentication and role-based authorization
- Database-backed workflow design
- Multi-user CRUD operations
- Full-stack integration using Blade and AdminLTE
- Building software around operational logic, not just UI screens

---

## Key Highlights

- Built a full-stack Laravel clinic workflow platform with role-based access for secretary, doctor, and admin users
- Structured appointment handling so front-desk actions and doctor workflows stay clearly separated
- Designed patient management around actual doctor-patient assignment logic
- Added administrative control for user management and access governance
- Used Laravel conventions to keep the project modular, readable, and easy to extend
- Modeled a realistic intake and medical coordination system instead of a basic demo app

---

## Use Case Diagram

![Use Case Diagram](./public/useCaseDiagram.png)

---

## Tech Stack

- **Laravel 9** — backend framework
- **PHP** — server-side development
- **MySQL** — relational database
- **Blade** — templating engine
- **AdminLTE** — dashboard interface
- **Bootstrap** — frontend styling
- **Composer** — PHP dependency management
- **NPM** — frontend package management

---

## Project Architecture

This system follows a standard Laravel full-stack structure with MVC separation.

- **Controllers** handle request flow and business actions
- **Models** manage database relationships and application entities
- **Blade views** render role-specific pages and forms
- **Migrations and seeders** manage database setup and test data
- **Routes** connect system actions to frontend workflows

The structure is designed to stay maintainable as more modules are added later such as billing, prescriptions, notifications, or analytics.

---

## Installation

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

### 3. Configure environment file

Create your `.env` file:

```bash
cp .env.example .env
```

Update the database configuration inside `.env`:

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

### 6. Seed demo data (optional)

```bash
php artisan db:seed
```

Check `database/seeders/DatabaseSeeder.php` if you want to see what records are inserted.

### 7. Build frontend assets

```bash
npm run dev
```

### 8. Start the server

```bash
php artisan serve
```

The application will run at:

```bash
http://127.0.0.1:8000
```

---

## Demo Credentials

If the database seeder is enabled, you can log in using these demo accounts:

| Role      | Email                                                             | Password |
| --------- | ----------------------------------------------------------------- | -------- |
| Admin     | [admin@clinictlemcen.com](mailto:admin@clinictlemcen.com)         | 123456   |
| Doctor    | [doctor@clinictlemcen.com](mailto:doctor@clinictlemcen.com)       | 123456   |
| Doctor    | [doctor2@clinictlemcen.com](mailto:doctor2@clinictlemcen.com)     | 123456   |
| Secretary | [secretary@clinictlemcen.com](mailto:secretary@clinictlemcen.com) | 123456   |

---

## Folder Structure

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

Important directories:

* `app/Models` — database entities
* `app/Http/Controllers` — backend request handling
* `resources/views` — Blade templates
* `routes/web.php` — application routes
* `database/migrations` — schema management
* `database/seeders` — sample/demo data

---

## Engineering Focus

What I like about this project is that it brings together three things I care about in software engineering:

* clear system structure
* practical workflow design
* controlled multi-user access

Even though the domain is healthcare, the engineering lessons are broader. This project is really about building a structured workflow product where different users interact with the same system differently, and the backend has to enforce that cleanly.

That is the part I find most valuable from an engineering perspective.

---

## Future Improvements

I can extend this system further with:

* patient medical history timeline
* prescription management
* billing and invoice support
* appointment reminders through email or SMS
* advanced search and filtering
* analytics dashboard for appointments and doctor activity
* audit logging for admin actions
* REST API support for third-party integration
* report export for patients and clinic operations

---

## Screenshots

You can add screenshots here to make the repository stronger.

Suggested sections:

* Login Page
* Secretary Dashboard
* Doctor Dashboard
* Appointment Creation Page
* Patient Management Page
* Admin User Management Page

---

## What This Project Shows

This project demonstrates:

* full-stack Laravel development
* role-based authorization
* backend-driven workflow design
* multi-user application architecture
* practical healthcare software modeling
* maintainable CRUD and dashboard system design

It is a strong project for showcasing backend engineering, Laravel development, and real-world application thinking.

---

## Acknowledgements

* [Laravel](https://laravel.com)
* [AdminLTE](https://adminlte.io/themes/v3/)

---

## License

This project is open-source and available under the MIT License.
