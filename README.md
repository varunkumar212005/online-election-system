# Online Election System

A beginner-friendly academic web application built with Python Flask and SQLite. It demonstrates user registration, password hashing, a sample ballot, one-vote-per-account validation and result counting.

## Features

- User registration and login
- Passwords stored as secure hashes using Werkzeug
- Sample candidate list
- One vote per account, enforced by a database uniqueness constraint
- Results page with vote totals
- Responsive HTML/CSS interface

## Technology stack

Python, Flask, SQLite, HTML, CSS, Jinja2

## Run locally

1. Install Python 3.10 or newer.
2. Open a terminal in this project folder.
3. Create and activate a virtual environment:

   **macOS/Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

   **Windows**
   ```bash
   py -m venv .venv
   .venv\\Scripts\\activate
   ```

4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
5. Start the application:
   ```bash
   python app.py
   ```
6. Open `http://127.0.0.1:5000` in your browser.

The SQLite database is created automatically on first run. Sample candidates are inserted automatically.

## Project structure

```text
online-election-system/
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── register.html
│   ├── login.html
│   ├── vote.html
│   └── results.html
└── static/
    └── style.css
```

## Important limitations

This is an educational demonstration, not a production election platform. It does not provide voter identity verification, anonymous ballot handling, auditability, election administration controls, CSRF protection, production secret management, or independent security certification. Do not use it for real elections or sensitive voting. Before deployment, set a strong secret key through an environment variable, disable debug mode, add CSRF protection, and conduct a security review.
