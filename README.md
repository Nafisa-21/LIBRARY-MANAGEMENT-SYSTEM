# RDBMS Library Management System

## Overview

**Library Management System** is a relational database project developed using Oracle SQL (PL/SQL). It simulates a real-world library system where users can borrow and return books or videos. The system supports three types of users: **Admins**, **Customers**, and **Employees**.

Admins have full control over the system, including user management and media inventory. Customers and employees can log in to rent or return media items and handle fines if they are late.

---

## Features

### 🔑 User Roles

- **Admin**:
  - Log in securely.
  - Add, update, and remove customers and employees.
  - View user information and outstanding fines.
  - Add, update, and remove books and videos.
- **Customer**:
  - Log in with username and password.
  - Rent and return books or videos.
  - View personal details and current fines.
- **Employee**:
  - Similar capabilities as customers.
  - Additional payroll and branch assignment information.

### 📚 Media Inventory

- Supports both books and videos.
- Tracks item status (available/borrowed), physical condition, and location.
- Calculates deby (late) and lost costs.

### 💼 Fine Management

- Automatically applies fines if media is returned after the due date.
- Allows users to pay fines partially or in full.
- Card status changes based on fine payment (active/blocked).

---

## Technical Highlights

- **Platform**: Oracle Database (PL/SQL)
- **Access**: Command-line based interaction
- **Database Objects Used**:
  - 9 Tables
  - 22 Stored Procedures
  - 3 Triggers
  - 1 User-Defined Object Type
  - Multiple cursors and sequences

---

## Database Structure

### Tables

- `Admin`: Stores admin login credentials.
- `Card`: Tracks card ID, status (active/blocked), and fine amounts.
- `Location`: Stores physical addresses of library branches.
- `Branch`: Contains branch names, locations, and contact numbers.
- `Customer`: Includes personal and account information.
- `Employee`: Includes employee details, branch assignment, and salary.
- `Book`: Tracks book metadata and availability.
- `Video`: Tracks video metadata and availability.
- `Rent`: Tracks rental records with rent and return dates.

### Procedures

- User login for admin, customer, and employee.
- Add, update, and view details for users.
- Add, view, and remove books/videos.
- Rent and return items with availability and fine updates.
- Pay fines and update card status.
- View all media via cursor.
- Handle media return conditions and overdue penalties.

### Triggers

- Auto-message on customer and employee creation.
- Fine modification on item return based on return date.

### Object Types

- `director_library`: Custom object to view enhanced employee details.

---

## Usage Summary

This system demonstrates how relational databases can manage real-world library operations, showcasing user access control, data consistency through triggers, and modular logic via PL/SQL procedures. It’s a compact example of how databases support transactional systems while enforcing business logic and integrity.

---

