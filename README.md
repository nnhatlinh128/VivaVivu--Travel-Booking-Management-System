# 🌍 VivaVivu - Travel Booking Management System | ASP.NET Core MVC

<p align="center">

A full-stack **Travel Booking Management System** built with **ASP.NET Core MVC** that enables users to browse tours, make online bookings, and complete secure payments through **VNPay, PayPal, and MoMo**.

Designed as an academic project to simulate a real-world online travel booking platform with integrated electronic payment gateways.

</p>

---

## 📑 Table of Contents

- [📖 About the Project](#-about-the-project)
- [🎯 Project Objectives](#-project-objectives)
- [✨ Key Features](#-key-features)
- [🛠 Technology Stack](#-technology-stack)
- [🏗 System Architecture](#-system-architecture)
- [🗄 Database Design](#-database-design)
- [💳 Electronic Payment Integration](#-electronic-payment-integration)
- [📸 System Screenshots](#-system-screenshots)
- [🚀 Getting Started](#-getting-started)
- [⚙ Configuration](#-configuration)
- [🌐 Live Demo](#-live-demo)

---

# 📖 About the Project

VivaVivu is a web-based **Travel Booking Management System** developed using **ASP.NET Core MVC**.

The project allows customers to search for travel tours, book tours online, and complete secure electronic payments through multiple payment gateways.

Besides customer functionalities, the system also provides an administration panel for managing tours, bookings, users, and business reports.

One of the major highlights of this project is the integration of **three electronic payment gateways**:

- 💙 VNPay
- 💙 PayPal
- 💙 MoMo

which simulate a real-world online payment workflow.

---

# 🎯 Project Objectives

This project aims to:

- Build a complete travel booking website.
- Simulate an online booking process.
- Integrate multiple electronic payment gateways.
- Apply ASP.NET Core MVC architecture.
- Practice Entity Framework Core with PostgreSQL.
- Implement authentication and authorization using ASP.NET Identity.
- Provide an administration dashboard for business management.

---

# ✨ Key Features

## 👤 Customer

- Register/Login
- Browse Tours
- Search Tours
- View Tour Details
- Book Tours
- Apply Discount
- Online Payment
    - VNPay
    - PayPal
    - MoMo
- View Booking History
- Booking Details
- Email Confirmation

---

## 👨‍💼 Administrator

- Dashboard
- Tour Management
- Category Management
- Booking Management
- User Management
- Revenue Statistics

---

# 🛠 Technology Stack

| Layer | Technologies | Purpose |
|-------|--------------|----------|
| ⚙️ **Backend** | ASP.NET Core MVC, C#, Entity Framework Core, ASP.NET Identity | Build business logic, authentication, and RESTful application flow |
| 🎨 **Frontend** | Razor Views, Bootstrap 5, HTML5, CSS3, JavaScript, jQuery | Build responsive user interfaces |
| 🗄️ **Database** | PostgreSQL, Supabase | Store application data |
| 💳 **Payment Gateway** | VNPay Sandbox, PayPal Sandbox, MoMo Sandbox | Process secure online payments |
| 📄 **Reporting** | QuestPDF, EPPlus | Export PDF invoices and Excel reports |
| 📝 **Logging** | Serilog | Application logging and monitoring |
| ☁️ **Deployment** | Render | Host the web application |

---

# 🏗 System Architecture

```
                 Users
                    │
                    ▼
      ASP.NET Core MVC Website
                    │
        Payment Controller
                    │
     ┌────────┬────────┬────────┐
     ▼        ▼        ▼
   VNPay    PayPal    MoMo
     │        │        │
     └────────┴────────┘
              │
       Return URL / Callback
              │
              ▼
      PostgreSQL Database
```

The application follows the **MVC architecture**, where Controllers handle requests, Models represent business entities, Views render the user interface, and Entity Framework Core manages database operations.

---

# 🗄 Database Design

The main entities include:

- Users
- Tours
- Categories
- Bookings
- BookingDetails
- Reviews

<img width="2810" height="1624" alt="supabase-schema-rlrzbhtrgvkxwvzzlmfw" src="https://github.com/user-attachments/assets/fc368f2a-c482-47b9-88c3-f590fbca0773" />

---

# 💳 Electronic Payment Integration

The system supports three electronic payment gateways.

| Gateway | Status |
|----------|:------:|
| VNPay | ✅ |
| PayPal | ✅ |
| MoMo | ✅ |

---

## Payment Workflow

```
Customer

↓

Book Tour

↓

Payment Controller

↓

Payment Gateway

↓

VNPay / PayPal / MoMo

↓

Return URL

↓

Update Booking

↓

Payment Success
```

---

## VNPay

- Redirect Payment
- Secure Signature Validation
- Payment Status Update

---

## PayPal

- REST API Integration
- Create Order
- Capture Order
- Payment Status Update

---

## MoMo

- Create Payment API
- HMAC SHA256 Signature
- QR Code / Pay URL
- Return URL Handling

---

# 📸 System Screenshots

## 🏠 Home Page

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 31 28" src="https://github.com/user-attachments/assets/c69aaa4e-cdfd-4ca9-a23b-91359b088f87" />

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 31 44" src="https://github.com/user-attachments/assets/ef39e701-a9db-47d2-be9c-a9fe177d838b" />

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 32 00" src="https://github.com/user-attachments/assets/9f059df8-8344-496a-8718-23220658618f" />


---

## 🔍 Tour Details

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 32 24" src="https://github.com/user-attachments/assets/2e83fac8-dbbc-4559-a5c4-72d643b04dd1" />

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 32 32" src="https://github.com/user-attachments/assets/e75216ed-12a6-451a-b729-1dfbdbc67648" />

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 32 54" src="https://github.com/user-attachments/assets/0cf2915a-6f08-493c-966d-143d97f20a32" />

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 33 01" src="https://github.com/user-attachments/assets/363af815-3464-4d39-8fb3-209560f1d4d7" />

---

## 📝 Booking Page

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 33 36" src="https://github.com/user-attachments/assets/00756e30-5dd8-46cc-b73f-5344e65e56f7" />

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 34 22" src="https://github.com/user-attachments/assets/31cce2c8-f77c-4ea9-be9d-128d3a4c0e77" />

<img width="1902" height="828" alt="Screenshot 2026-07-09 at 22 21 32" src="https://github.com/user-attachments/assets/db3c906b-b6ef-4d35-89b4-7da18105ccd9" />

---

## 💳 VNPay Payment

<img width="607" height="310" alt="Screenshot 2026-07-09 at 22 14 41" src="https://github.com/user-attachments/assets/726c1ecd-10d6-4601-8edf-13486b05b7a3" />

---

## 💙 PayPal Payment

<img width="611" height="307" alt="Screenshot 2026-07-09 at 22 14 56" src="https://github.com/user-attachments/assets/c26ff746-6234-414c-a3eb-0c889881c222" />

---

## 💗 MoMo Payment

<img width="604" height="304" alt="Screenshot 2026-07-09 at 22 15 08" src="https://github.com/user-attachments/assets/79fb13ae-20aa-4b9c-a52b-3699845e5508" />

---

## 📋 Booking Success

<img width="1696" height="857" alt="Screenshot 2026-06-05 at 11 34 51" src="https://github.com/user-attachments/assets/a7fda28d-cfb1-4eab-a66c-aef23b3ab23d" />

---

# 🚀 Getting Started

## Clone Repository

```bash
git clone https://github.com/nnhatlinh128/VivaVivu--Travel-Booking-Management-System.git
```

---

## Restore Packages

```bash
dotnet restore
```

---

## Update Database

```bash
dotnet ef database update
```

---

## Run Project

```bash
dotnet run
```

---

# ⚙ Configuration

Configure the following settings before running the project:

- PostgreSQL Connection String
- Email Settings
- VNPay Sandbox
- PayPal Sandbox
- MoMo Sandbox

> ⚠️ Sensitive information such as API keys and secrets should be stored using Environment Variables or Secret Manager instead of committing them to GitHub.

---

# 🌐 Live Demo

🌍 Website

```
https://vivavivu-travel.onrender.com
```




