# Multi-Factor Authentication Project

## Overview

This project is a Multi-Factor Authentication (MFA) web application developed using Flask and SQLite. The main goal of the project is to improve account security by implementing multiple verification layers instead of relying only on a password.

The application uses Email OTP, WhatsApp OTP, and Google Authenticator (TOTP) to verify user identity during registration and login.

This project was developed as part of learning secure authentication mechanisms and cybersecurity concepts.

---

## Features

* User Registration
* User Login
* Email OTP Verification
* WhatsApp OTP Verification
* Google Authenticator Integration
* Password Reset via Email
* Secure Password Hashing
* QR Code Generation for TOTP Setup
* Account Suspension After Multiple Failed Login Attempts
* Session Management
* SQLite Database Storage

---

## Technologies Used

### Backend

* Python
* Flask
* Flask-Mail
* Flask-SQLAlchemy
* Flask-Migrate

### Database

* SQLite

### Authentication

* PyOTP
* Google Authenticator

### Communication Services

* Gmail SMTP
* UltraMsg WhatsApp API

### Frontend

* HTML
* CSS
* JavaScript

---

## Project Workflow

### Registration

1. User enters name, email, phone number, and password.
2. Email OTP is sent to the registered email address.
3. WhatsApp OTP is sent to the registered mobile number.
4. User verifies both OTPs.
5. Google Authenticator QR code is generated.
6. User scans the QR code and verifies the TOTP code.
7. Account is created successfully.

### Login

1. User enters email and password.
2. Password is verified.
3. User selects an additional authentication method.
4. Verification is completed using WhatsApp OTP or Google Authenticator.
5. User gains access to the system.

---

## Security Features

* Passwords are stored using hashing.
* Multiple authentication factors are required.
* Password reset links expire automatically.
* Brute-force protection through temporary account suspension.
* Session-based authentication handling.
* Time-based One-Time Password (TOTP) implementation.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/your-username/MFA.git
cd MFA
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Virtual Environment

Windows:

```bash
venv\Scripts\activate
```

Linux/macOS:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install flask flask_sqlalchemy flask_mail flask_migrate pyotp qrcode requests werkzeug
```

### Run Application

```bash
python app.py
```

Open:

```text
http://127.0.0.1:5000
```

---

## Project Structure

```text
MFA/
│
├── static/
├── templates/
├── app.py
├── config.py
├── README.md
└── database.db
```

---

## Future Improvements

* SMS OTP Integration
* Biometric Authentication
* JWT-Based Authentication
* OAuth Login (Google/GitHub)
* Admin Dashboard
* User Activity Logs

---

## Author

Ujjwal Shakya

Integrated B.Tech + M.Tech (Cyber Security)

National Forensic Sciences University (NFSU), Gandhinagar

Academic Session: 2023–2028

---

## Disclaimer

This project was developed for educational and learning purposes. API credentials, email passwords, and tokens should never be hardcoded in production environments. Environment variables and secure secret management solutions should be used instead.
