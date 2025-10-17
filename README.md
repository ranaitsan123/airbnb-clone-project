# 🏡 Airbnb Clone Backend – Solo Dev Project

A **full-stack-ready backend system** for an Airbnb-like platform, built and managed entirely by a **solo developer**.  
This project showcases **end-to-end ownership** of backend development, API security, database architecture, and CI/CD pipeline design — fully aligned with modern **DevSecOps practices**.

---

## 🙋‍♂️ About Me

🎓 **Master’s Student in Intelligent Systems Engineering**  
📚 **Specializing in Systems, Networking, and Cloud**  
🛡️ **Passionate about Cybersecurity and DevSecOps**  
💻 **Strong foundation in Software Engineering and Backend Development**

---

## 🛠️ Technology Stack

| Technology | Purpose |
|-------------|----------|
| **Django** | Backend framework for rapid development and clean, pragmatic design |
| **MySQL** | Relational database for structured data storage |
| **GraphQL** | Efficient API querying *(optional)* |
| **Docker** | Containerization for consistent development & deployment |
| **GitHub Actions** | CI/CD pipelines for automation |
| **JWT / OAuth2** | Secure API authentication |
| **Bandit / pylint / pytest** | Security linting, static analysis, and testing |

---

## 🗂️ Project Scope

As a solo developer, I handled the **entire development lifecycle**:

✅ Backend API architecture & implementation  
✅ Relational database schema design  
✅ RESTful API + (optional GraphQL endpoint)  
✅ Security enforcement (auth, access control, input validation)  
✅ CI/CD pipeline with GitHub Actions & Docker  
✅ Documentation and repository management  

---

## 📐 Database Design

### Entities & Relationships

| Entity | Fields | Relations |
|---------|---------|------------|
| **User** | id, name, email, password_hash, role | Has many bookings, reviews |
| **Property** | id, title, location, host_id | Belongs to User (host), has many bookings |
| **Booking** | id, user_id, property_id, start_date, end_date | Belongs to user and property |
| **Review** | id, user_id, property_id, rating, comment | One-to-one with booking |
| **Payment** | id, booking_id, amount, status | One-to-one with booking |

---

## 🔐 API Security Measures

| Measure | Purpose |
|----------|----------|
| **JWT Authentication** | Protect API endpoints and maintain secure sessions |
| **Role-based Authorization** | Prevent unauthorized access (e.g., guests editing listings) |
| **Rate Limiting (via Django middleware)** | Prevent API abuse and DDoS attacks |
| **Input Validation & Sanitization** | Protect against SQL injection, XSS |
| **HTTPS (development via SSL)** | Encrypted traffic (production-ready setup) |
| **Security Scanning (Bandit)** | Python code vulnerability analysis during CI |

---

## 🔄 CI/CD Pipeline Overview

| Step | Tool | Description |
|------|------|-------------|
| **Linting** | pylint / black | Enforce code quality |
| **Security Scanning** | bandit | Catch known security issues |
| **Testing** | pytest | Run unit and integration tests |
| **Docker Build** | Dockerfile | Containerized application for staging/prod |
| **Deploy Pipeline** | GitHub Actions | Automate build/test/push workflow |

✅ **Automated on every push to `main` branch**

---

## 🌟 Feature Breakdown

| Feature | Description |
|----------|-------------|
| **User Registration/Login** | Secure account creation and session management |
| **Property Listings** | Hosts can create, update, and delete properties |
| **Booking Engine** | Guests can book properties and view booking history |
| **Payments (Mock)** | Simulated payment flow with success/failure status |
| **Review System** | Leave reviews after bookings |
| **Admin View (Optional)** | View stats, users, and properties (secured endpoint) |

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/yourusername/airbnb-clone-project.git

# Set up virtual environment
python3 -m venv venv && source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env

# Run migrations
python manage.py migrate

# Start the dev server
python manage.py runserver
```

---

## 📌 Project Status

- ✅ Backend initialized with Django  
- ✅ Database schema designed  
- ✅ Auth + Role-based access implemented  
- ✅ REST API endpoints secured  
- ✅ CI/CD pipeline live with GitHub Actions  
- ✅ API tested (unit & integration)  
- 🔍 Final peer/manual review pending  

---

## 🔗 Links

- **GitHub Repository:** [https://github.com/ranaitsan123/airbnb-clone-project](https://github.com/yourusername/airbnb-clone-project)  
- **Review Link:** _(Add link here)_

---

## 🧠 Final Thoughts

As a solo developer, this project allowed me to practice real-world **DevSecOps workflows**, build a **secure backend system from scratch**, and **deploy confidently** using CI/CD automation.  
It’s a step forward in my journey toward becoming a **Full-Stack DevSecOps Engineer**.
