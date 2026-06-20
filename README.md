# Code Style Enforcer

## Motto

**"A teammate that never forgets your standards."**

---

# Overview

Code Style Enforcer is an AI-powered code review assistant that helps development teams maintain consistent coding standards.

Unlike traditional linters that rely on static configuration files, Code Style Enforcer stores coding standards in persistent memory using Parcle and applies them when reviewing code snippets.

Developers can paste JavaScript code into the application and instantly receive:

- Style violations
- Rule explanations
- Suggested fixes
- Team-standard enforcement

---

# Problem Statement

Development teams often define coding standards but fail to enforce them consistently.

Traditional linters:

- Require manual configuration
- Cannot explain rules intelligently
- Do not remember team-specific conventions
- Cannot leverage persistent memory

This project solves that problem by combining AI-style memory with automated code analysis.

---

# Features

### Rule Enforcement

The application checks code against team standards:

- camelCase Naming
- No console.log Statements
- Function Comment Requirement
- No Hardcoded Secrets

---

### Intelligent Feedback

Each violation includes:

- Rule Name
- Suggested Fix

Example:

```text
Rule: Use camelCase
Fix: Replace snake_case with camelCase
```

---

### Persistent Memory

Coding standards are stored in Parcle memory and retrieved whenever code is analyzed.

This allows the system to remember team standards across sessions.

---

# Architecture

```text
+------------------+
| React Frontend   |
+--------+---------+
         |
         |
         v
+------------------+
| Flask Backend    |
+--------+---------+
         |
         |
         v
+------------------+
| Checker Engine   |
+--------+---------+
         |
         |
         v
+------------------+
| Parcle Memory    |
+------------------+
```

---

# Technology Stack

## Frontend

- React
- Vite
- Axios

## Backend

- Python
- Flask
- Flask-CORS

## Memory Layer

- Parcle

---

# Tool Integration

## Parcle

Parcle enables persistent memory by storing team coding standards and retrieving them whenever code is analyzed, ensuring consistent rule enforcement across sessions.

Stored information:

- Coding standards
- Team rules
- Check history
- Memory retrieval

Example Rule:

```text
Variables and functions must use camelCase.
```

When code is submitted:

1. Rules are retrieved from Parcle
2. Code is analyzed
3. Violations are returned
4. Results are displayed to the user

---

## Enter Pro

Enter Pro was used for:

- Planning the project
- Rapid prototyping
- Application generation
- Deployment assistance

---

# Project Structure

```text
code-style-enforcer/

├── backend
│   ├── app.py
│   ├── checker.py
│   ├── server.js
│   ├── test-parcle.py
│   ├── package.json
│   ├── package-lock.json
│   ├── .env
│   └── __pycache__
│
├── frontend
│   ├── public
│   │   ├── favicon.svg
│   │   └── icons.svg
│   │
│   ├── src
│   │   ├── assets
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── package.json
│   ├── package-lock.json
│   ├── vite.config.js
│   ├── eslint.config.js
│   └── index.html
│
├── .env
├── README.md
└── .gitignore
```
---

# Installation

## Clone Repository

```bash
git clone <repository-url>
```

---

## Backend Setup

```bash
cd backend

pip install -r requirements.txt

python app.py
```

Server runs on:

```text
http://localhost:5000
```

---

## Frontend Setup

```bash
cd frontend

npm install

npm run dev
```

Frontend runs on:

```text
http://localhost:5173
```

---

# Demo

Sample Input:

```javascript
const user_name = "John";
const api_key = "12345";

console.log(user_name);

function calculate_total(a, b) {
  return a + b;
} 
```

Expected Output:

```text
Use camelCase
No console.log
Missing function comment
Hardcoded secret detected

```

---

Deployment

Frontend:
https://code-style-enforcer.vercel.app/

Backend API:
https://code-style-enforcer.onrender.com/

Hosting:
- Frontend deployed on Vercel
- Backend deployed on Render

The application is publicly accessible through cloud-hosted services.

# Future Improvements

- Auto-fix functionality
- AI-generated code corrections
- Additional language support
- Team-specific custom rule creation
- Advanced memory retrieval
- GitHub integration

---

# Hackathon Submission Checklist

✅ GitHub Repository

✅ Demo Video

✅ Live Project

✅ Parcle Integration

✅ Enter Pro Integration

✅ Documentation

---

# Team

Developed as part of the Sentient Engineer Hackathon Challenge.

**Code Style Enforcer**
*A teammate that never forgets your standards.*
