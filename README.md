# ☕ Urban Brew Cafe — Cafe Management System

A modern, responsive **Cafe Management System** built with **PHP, MySQL, HTML, CSS and JavaScript**.

Urban Brew Cafe provides a complete digital experience for customers to explore the cafe, create an account, place food and beverage orders, reserve tables and submit feedback. An integrated **Admin Control Panel** allows cafe administrators to manage users, orders, reservations and customer feedback.

---

## 📌 Project Overview

**Urban Brew Cafe** is a web-based cafe management system designed for cafes and small restaurants.

The system has two major sections:

### 👤 Customer Website

Customers can:

* View cafe information
* Explore the menu
* Register an account
* Login securely
* Place online orders
* Choose dine-in, takeaway or delivery
* Reserve a table
* Submit feedback and ratings
* Manage their profile
* Logout securely

### 🔐 Admin Panel

Administrators can:

* Login through a dedicated admin portal
* View dashboard statistics
* Monitor total users
* Manage customer orders
* Manage table reservations
* View customer feedback
* Manage registered users
* Track pending orders and reservations
* Update order/reservation statuses

---

# ✨ Features

## 🏠 Customer Website

### Home Page

* Cafe hero section
* Cafe introduction
* About Urban Brew
* Menu categories
* Photo gallery
* Team section
* Customer feedback
* Cafe information
* Responsive navigation

### 🍵 Menu

The system includes:

* Espresso
* Cappuccino
* Flat White
* Caramel Latte
* Matcha Latte
* Cold Brew
* Frappuccino
* Butter Croissant
* Avocado Toast
* Eggs Benedict

Menu filtering is available by:

* All
* Coffee
* Cold Drinks
* Food

---

## 🛒 Online Ordering

Customers can place orders using:

* Customer name
* Mobile number
* Menu item
* Quantity
* Order type
* Delivery address
* Payment method
* UPI reference

### Order Types

* 🍽️ Dine In
* 🛍️ Takeaway
* 🛵 Home Delivery

A **₹30 delivery charge** is automatically added for home delivery within Kolhapur.

The system validates:

* Customer name
* Mobile number
* Menu item
* Quantity
* Delivery address when required

---

## 📅 Table Reservation

Customers can reserve a table by providing:

* Name
* Mobile number
* Number of guests
* Date
* Time
* Special request

Reservation status can be:

* Pending
* Approved
* Cancelled

---

## 👤 User Authentication

The customer authentication system supports:

* User registration
* Login
* Logout
* Session-based authentication
* Password hashing
* Password verification
* Protected user pages

Passwords are stored using PHP's `password_hash()` mechanism rather than plain text.

---

# 🔐 Admin Control Panel

The admin dashboard provides an overview of cafe activity.

### Dashboard Statistics

The dashboard displays:

* Total Users
* Total Orders
* Total Reservations
* Total Feedback
* Pending Orders
* Pending Reservations

### Admin Modules

```text
Admin
├── Dashboard
├── Orders
├── Reservations
├── Users
├── Feedback
└── Logout
```

Only authenticated administrators can access protected admin pages.

---

# 🗄️ Database

The project uses **MySQL**.

Database name:

```text
urbanbrew_db
```

### Database Tables

```text
admins
users
reservations
orders
feedback
```

### Relationship Overview

```text
users
  │
  ├── reservations
  │
  ├── orders
  │
  └── feedback

admins
  │
  └── Admin Panel
```

Foreign keys are used between customer-related records and the `users` table.

---

# 🛠️ Technology Stack

| Technology        | Purpose                           |
| ----------------- | --------------------------------- |
| PHP               | Backend / Server-side Programming |
| MySQL             | Database                          |
| HTML5             | Page Structure                    |
| CSS3              | UI / Styling                      |
| JavaScript        | Client-side Interactions          |
| PDO               | Database Connectivity             |
| Sessions          | Authentication                    |
| Google Fonts      | Typography                        |
| Unsplash / Pexels | Demo Images                       |

---

# 📂 Project Structure

```text
urbanbrew/
│
├── index.php
├── login.php
├── register.php
├── logout.php
├── profile.php
├── order.php
├── reserve.php
├── feedback.php
├── config.php
│
├── includes/
│   ├── auth.php
│   ├── header.php
│   └── footer.php
│
├── admin/
│   ├── login.php
│   ├── logout.php
│   ├── dashboard.php
│   ├── orders.php
│   ├── reservations.php
│   ├── users.php
│   ├── feedback.php
│   │
│   └── includes/
│       ├── admin_header.php
│       └── admin_footer.php
│
├── assets/
│   ├── css/
│   │   ├── style.css
│   │   └── admin.css
│   │
│   └── js/
│       └── main.js
│
└── sql/
    └── urbanbrew.sql
```

---

# 💻 Requirements

Before installing the project, make sure you have:

* PHP 7.4+ or newer
* MySQL 5.7+ / MariaDB
* Apache Server
* XAMPP / WAMP / LAMP
* Modern web browser

Recommended development environment:

```text
XAMPP
Apache
MySQL
PHP
phpMyAdmin
```

---

# 🚀 Installation

## Step 1 — Install XAMPP

Install XAMPP and start:

```text
Apache
MySQL
```

---

## Step 2 — Copy Project

Copy the `urbanbrew` folder into:

```text
C:\xampp\htdocs\
```

The final structure should be:

```text
C:\xampp\htdocs\urbanbrew\
```

---

## Step 3 — Create Database

Open:

```text
http://localhost/phpmyadmin
```

Create/import the database using:

```text
sql/urbanbrew.sql
```

The SQL file creates:

```text
urbanbrew_db
```

and its required tables.

---

# ⚙️ Database Configuration

Open:

```text
config.php
```

Default configuration:

```php
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'urbanbrew_db');
```

If your MySQL credentials are different, update these values.

Also update:

```php
define('SITE_URL', 'http://localhost/urbanbrew');
```

if your installation uses a different URL.

---

# 🌐 Run the Project

After starting Apache and MySQL, open:

```text
http://localhost/urbanbrew/
```

You should see the Urban Brew Cafe website.

---

# 🔑 Admin Login

Admin login page:

```text
http://localhost/urbanbrew/admin/login.php
```

### Default Credentials

```text
Email: admin@urbanbrew.com
Password: password
```

> ⚠️ Change the default admin password before using the project in a real production environment.

---

# 👤 Customer Registration

Customer registration:

```text
http://localhost/urbanbrew/register.php
```

After registration, users can login from:

```text
http://localhost/urbanbrew/login.php
```

---

# 🔄 Application Flow

## Customer Flow

```text
Visit Website
      ↓
Explore Cafe
      ↓
View Menu
      ↓
Register / Login
      ↓
Place Order
      ↓
Choose Order Type
      ↓
Order Confirmation
```

### Reservation Flow

```text
Customer
   ↓
Reserve Table
   ↓
Enter Date & Time
   ↓
Enter Guest Details
   ↓
Submit Reservation
   ↓
Pending
   ↓
Admin Review
   ↓
Approved / Cancelled
```

### Admin Flow

```text
Admin Login
     ↓
Dashboard
     ↓
 ┌───────────────┐
 │ Users         │
 │ Orders        │
 │ Reservations  │
 │ Feedback      │
 └───────────────┘
```

---

# 🔒 Security Features

The project includes several basic security practices:

* Password hashing using PHP
* Password verification using `password_verify()`
* PDO prepared statements
* Session-based authentication
* Admin access protection
* Customer access protection
* HTML output sanitization
* Server-side form validation
* MySQL foreign-key relationships
* UTF-8 / UTF8MB4 database support

---

# 💳 Payment Support

The current system supports payment method selection:

```text
UPI
Cash
Card
```

For UPI orders, an optional UPI reference can be stored.

> Note: This project does not currently implement a live payment gateway such as Razorpay or Stripe. Payment gateway integration can be added in a future version.

---

# 📊 Admin Dashboard

The admin dashboard provides quick visibility into cafe operations.

Example metrics:

```text
Total Users
Total Orders
Total Reservations
Total Feedback
Pending Orders
Pending Reservations
```

The dashboard also displays:

* Recent orders
* New users
* Order status
* Reservation status

---

# 🎨 UI / Design

The website uses a cafe-inspired visual design with:

* Responsive layouts
* Modern cards
* Coffee-themed typography
* Hero sections
* Menu tabs
* Gallery
* Forms
* Alerts
* Admin dashboard tables
* Mobile-friendly styling

Fonts used include:

```text
Playfair Display
Lato
```

---

# 🧪 Testing Checklist

### Customer

* [ ] Homepage loads
* [ ] Registration works
* [ ] Login works
* [ ] Logout works
* [ ] Profile opens
* [ ] Order can be placed
* [ ] Delivery address validation works
* [ ] ₹30 delivery fee works
* [ ] Table reservation works
* [ ] Feedback submission works

### Admin

* [ ] Admin login works
* [ ] Dashboard loads
* [ ] User list works
* [ ] Order management works
* [ ] Reservation management works
* [ ] Feedback management works
* [ ] Admin logout works

### Database

* [ ] Database imported successfully
* [ ] Tables created
* [ ] User records inserted
* [ ] Orders stored correctly
* [ ] Reservations stored correctly
* [ ] Feedback stored correctly

---

# 🐛 Common Problems

## Database Connection Failed

Check:

```text
DB_HOST
DB_USER
DB_PASS
DB_NAME
```

Also make sure MySQL is running.

---

## Page Not Found

Make sure the project is inside:

```text
C:\xampp\htdocs\urbanbrew\
```

Then open:

```text
http://localhost/urbanbrew/
```

---

## Admin Login Not Working

Make sure the SQL file was imported correctly and the `admins` table contains the default administrator record.

---

# 🔮 Future Enhancements

The following features can be added in future versions:

* Razorpay payment gateway
* Real-time order tracking
* Email notifications
* SMS notifications
* WhatsApp notifications
* Shopping cart
* Multiple-item orders
* Dynamic database-driven menu
* Food image management
* Coupon and discount system
* Inventory management
* Sales reports
* Revenue analytics
* Staff accounts
* Role-based admin permissions
* Password reset
* Email verification
* Customer order history
* Reservation availability checking
* QR-code based table ordering
* Invoice generation
* Production-grade security hardening

---

# 📜 License

This project is intended for **educational, academic and demonstration purposes**.

You may modify and extend the project according to your requirements.

---

# 👨‍💻 Project Information

**Project Name:** Urban Brew Cafe Management System

**Type:** Web-Based Cafe Management System

**Backend:** PHP

**Database:** MySQL

**Frontend:** HTML5, CSS3, JavaScript

**Architecture:** PHP + MySQL

---

# 🤝 Developer

### Abrar Patel

**Web Developer & Project Developer**

I develop academic projects, web applications and professional websites using modern technologies.

### 🌐 AP Webcraft

For academic projects, custom software solutions and professional website development:

[AP Webcraft — Official Website](https://apwebcraft22.netlify.app/?utm_source=chatgpt.com)

### 💼 LinkedIn

Connect with me professionally:

[Abrar Patel — LinkedIn](https://www.linkedin.com/in/abrar-patel-93083340a?utm_source=chatgpt.com)

---

# ❤️ Urban Brew Cafe

> **Where Every Cup Tells a Story.**

A digital cafe experience designed to connect customers, orders, reservations and cafe administration in one simple platform.

---

### ⭐ If you find this project useful

Feel free to connect with the developer on LinkedIn and explore more projects and services through **AP Webcraft**.

**Made with ❤️ by Abrar Patel | AP Webcraft**
