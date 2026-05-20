# PRODUCT REQUIREMENTS DOCUMENT (PRD)

# Wisdom Expense Manager

### Version: MVP V1.0

### Client: Wisdom The Global School

### Project Type: Web-Based Expense Management System

### Prepared By: Software Development Team

---

# 1. Project Overview

## Product Summary

Wisdom Expense Manager is a modern web-based financial management application designed specifically for school expense tracking and financial monitoring.

The system will replace manual bookkeeping and scattered spreadsheets with a centralized digital platform where administrators and accountants can efficiently manage school expenses, categories, vendors, reports, and financial insights.

This version focuses only on the essential features shown in the provided dashboard UI reference and will serve as the Minimum Viable Product (MVP).

The application will feature:

* Modern dark-themed dashboard
* Expense tracking system
* Expense analytics
* Vendor management
* Financial reporting
* Secure authentication
* Responsive admin interface

---

# 2. Project Goals

## Primary Goals

* Simplify expense management operations
* Digitize school financial records
* Provide quick financial overview through dashboards
* Improve financial transparency
* Reduce manual calculation errors
* Enable faster reporting
* Create a scalable system foundation for future expansion

---

# 3. Target Users

## 3.1 Admin

### Description

School management or senior administrative users.

### Responsibilities

* Monitor financial activities
* Manage expenses
* Manage categories
* Manage vendors
* Access reports
* Monitor dashboard analytics

---

## 3.2 Accountant

### Description

Staff responsible for handling daily expenses.

### Responsibilities

* Add expenses
* Edit expenses
* View reports
* Manage vendors
* Monitor dashboard

---

## 3.3 Viewer

### Description

Read-only access users.

### Responsibilities

* View dashboard
* View reports
* Monitor analytics

---

# 4. User Roles & Permissions

| Module            | Admin | Accountant | Viewer |
| ----------------- | ----- | ---------- | ------ |
| Dashboard         | Yes   | Yes        | Yes    |
| Add Expenses      | Yes   | Yes        | No     |
| Edit Expenses     | Yes   | Yes        | No     |
| Delete Expenses   | Yes   | Yes        | No     |
| Manage Categories | Yes   | No         | No     |
| Manage Vendors    | Yes   | Yes        | No     |
| View Reports      | Yes   | Yes        | Yes    |
| Export Reports    | Yes   | Yes        | No     |
| Settings          | Yes   | Limited    | No     |

---

# 5. Core Modules

---

# 5.1 Authentication Module

## Objective

Provide secure login access for authorized users.

## Features

### Login System

* Username/email login
* Password authentication
* Session handling
* Logout functionality

### Security Features

* Password hashing
* Session protection
* Unauthorized route blocking
* Invalid login handling

## Validation Rules

* Empty credentials not allowed
* Incorrect login shows error message
* Passwords never stored in plain text

---

# 5.2 Dashboard Module

## Objective

Provide a quick overview of school financial activities.

## UI Style

* Dark modern dashboard
* Sidebar navigation
* Analytics cards
* Interactive charts

---

## Dashboard Components

### Summary Cards

#### Total Expenses

Displays:

* Total expenses amount

#### Spend vs Budget

Displays:

* Current spending percentage

#### Active Vendors

Displays:

* Total active vendors

---

## Analytics Charts

### Monthly Expense Trend

Bar chart displaying:

* Monthly spending trends

### Expense Distribution

Displays:

* Category-wise expense analysis

---

## Recent Activity Section

Displays:

* Latest expense entries
* Recent updates
* Recent vendor activities

---

# 5.3 Expense Management Module

## Objective

Manage all school expense records.

---

## Features

### Add Expense

Users can create new expense records.

### Edit Expense

Users can modify existing expenses.

### Delete Expense

Authorized users can remove expense entries.

### Expense Listing

Displays all expenses in a responsive table.

### Search & Filters

Users can filter by:

* Category
* Vendor
* Date
* Payment method

---

## Expense Fields

| Field          | Type          | Validation    |
| -------------- | ------------- | ------------- |
| Title          | Text          | Required      |
| Amount         | Decimal       | Positive only |
| Category       | Dropdown      | Required      |
| Vendor         | Dropdown/Text | Optional      |
| Payment Method | Dropdown      | Required      |
| Description    | Textarea      | Optional      |
| Expense Date   | Date          | Required      |

---

## Supported Payment Methods

* Cash
* Bank Transfer
* UPI
* Card
* Cheque

---

# 5.4 Categories Module

## Objective

Organize expenses into manageable groups.

---

## Features

### Add Category

Admin can create categories.

### Edit Category

Admin can modify categories.

### Delete Category

Admin can remove categories.

---

## Default Categories

* Salary
* Electricity
* Water
* Internet
* Stationery
* Events
* Transport
* Repairs
* Miscellaneous

---

# 5.5 Vendors Module

## Objective

Maintain vendor/supplier information.

---

## Features

### Add Vendor

Create vendor records.

### Edit Vendor

Update vendor details.

### Delete Vendor

Remove vendors.

### Vendor Listing

View all vendors.

---

## Vendor Fields

| Field          | Type     |
| -------------- | -------- |
| Vendor Name    | Text     |
| Contact Number | Text     |
| Email          | Text     |
| Address        | Textarea |

---

# 5.6 Reports Module

## Objective

Generate financial summaries and downloadable reports.

---

## Report Types

### Monthly Reports

Includes:

* Monthly total expenses
* Category breakdown

### Category Reports

Includes:

* Expenses grouped by category

### Custom Date Range Reports

User selects:

* Start date
* End date

---

## Export Formats

* PDF
* CSV

---

# 5.7 Settings Module

## Objective

Manage basic user preferences.

---

## Features

### Profile Settings

* Update profile information

### Password Management

* Change password

### Theme Settings (Optional)

* Dark/light mode toggle

---

# 6. Functional Requirements

---

# Authentication Requirements

* Users must login before accessing protected routes
* Sessions must remain secure
* Unauthorized access must redirect to login page

---

# Dashboard Requirements

* Dashboard loads dynamically
* Cards display updated values
* Charts reflect latest expenses

---

# Expense Requirements

* Expense amount must always be positive
* Required fields must validate properly
* Expense records must update instantly

---

# Categories Requirements

* Categories must be manageable by admin only
* Deleted categories should not affect old expense records

---

# Vendor Requirements

* Vendor records should be editable
* Vendor listing must support search

---

# Reports Requirements

* Reports generate dynamically
* Exported files should download correctly
* Filters must work accurately

---

# 7. Non-Functional Requirements

---

# Security

System must include:

* Password hashing
* Session protection
* SQL injection prevention
* CSRF protection
* Input validation

---

# Performance

System should:

* Load dashboard quickly
* Handle large expense lists efficiently
* Use optimized database queries

---

# Scalability

Architecture should support:

* Future API integration
* Multi-school support
* Cloud deployment

---

# Usability

Application should:

* Be mobile responsive
* Provide intuitive navigation
* Use clean dashboard layouts

---

# Reliability

System should:

* Handle errors properly
* Prevent data corruption
* Maintain stable sessions

---

# 8. Technology Stack

## Backend

* Python
* Flask

---

## Frontend

* HTML5
* CSS3
* JavaScript
* Bootstrap 5

---

## Database

* SQLite

---

## Charts & UI

* Chart.js
* Font Awesome

---

# 9. Database Design

---

# Users Table

Stores:

* User credentials
* Roles
* Account status

### Fields

* id
* username
* email
* password_hash
* role
* created_at

---

# Categories Table

Stores:

* Expense categories

### Fields

* id
* category_name
* status
* created_at

---

# Vendors Table

Stores:

* Vendor details

### Fields

* id
* vendor_name
* contact_number
* email
* address
* created_at

---

# Expenses Table

Stores:

* Expense records

### Fields

* id
* title
* amount
* category_id
* vendor_id
* payment_method
* description
* expense_date
* created_by
* created_at

---

# 10. System Architecture

## Architecture Style

* Modular Flask architecture
* MVC-inspired structure
* Role-based route protection
* SQLite relational database structure

---

# 11. UI/UX Requirements

---

# Design Style

The application should follow:

* Modern admin dashboard UI
* Dark theme design
* Professional financial dashboard appearance
* Responsive layout

---

# Layout Components

## Sidebar

Contains:

* Dashboard
* Expenses
* Categories
* Vendors
* Reports
* Settings
* Logout

---

## Top Navigation Bar

Contains:

* Search bar
* User profile section
* Notifications icon

---

## Dashboard Cards

Modern glassmorphism style cards with:

* Statistics
* Icons
* Highlights

---

## Tables

Responsive tables with:

* Pagination
* Search
* Filters

---

# Color Palette

| Color     | Usage              |
| --------- | ------------------ |
| Dark Navy | Main background    |
| Neon Blue | Primary highlights |
| White     | Text               |
| Gray      | Secondary sections |
| Green     | Success            |
| Red       | Error              |

---

# 12. Project File Structure

```plaintext
expense_manager/
│
├── app/
│   ├── static/
│   │   ├── css/
│   │   │   └── style.css
│   │   │
│   │   ├── js/
│   │   │   └── script.js
│   │   │
│   │   ├── img/
│   │   └── uploads/
│   │
│   ├── templates/
│   │   ├── auth/
│   │   │   └── login.html
│   │   │
│   │   ├── dashboard/
│   │   │   └── dashboard.html
│   │   │
│   │   ├── expenses/
│   │   ├── categories/
│   │   ├── vendors/
│   │   ├── reports/
│   │   └── settings/
│   │
│   ├── routes/
│   ├── models/
│   ├── forms/
│   ├── utils/
│   └── __init__.py
│
├── database/
│   └── database.db
│
├── config.py
├── requirements.txt
├── run.py
└── README.md
```

---

# 13. Development Phases

---

# Phase 1 — Project Setup

## Tasks

* Flask setup
* Database setup
* Authentication system
* Base UI structure

---

# Phase 2 — Expense System

## Tasks

* Expense CRUD
* Categories module
* Vendors module
* Search & filters

---

# Phase 3 — Dashboard & Reports

## Tasks

* Dashboard analytics
* Reports generation
* PDF/CSV export
* Chart integration

---

# Phase 4 — Finalization

## Tasks

* Testing
* UI polishing
* Performance optimization
* Deployment preparation

---

# 14. Security Requirements

System must:

* Hash passwords securely
* Prevent unauthorized access
* Validate all forms
* Protect sessions
* Prevent SQL injection
* Implement CSRF protection

---

# 15. Future Scope

Future versions may include:

* Mobile application
* AI analytics
* Budget planning
* Email notifications
* Multi-school support
* Cloud deployment
* Approval workflows

---

# 16. Success Metrics

Project success will be measured by:

* Faster expense entry
* Improved financial visibility
* Reduced paperwork
* Accurate reporting
* Faster report generation
* Easy user adoption

---

# 17. Final Deliverables

## Deliverables

* Complete Flask web application
* SQLite database
* Responsive frontend UI
* Dashboard analytics
* Reports module
* Deployment-ready source code
* Documentation

---

# 18. Conclusion

Wisdom Expense Manager MVP will provide a centralized and professional expense management solution for Wisdom The Global School.

The system will:

* Simplify expense management
* Improve reporting efficiency
* Increase financial transparency
* Provide modern dashboard analytics
* Create a scalable foundation for future ERP expansion
