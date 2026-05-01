# 🏦 Streamlit Bank — A Lightweight Banking System

## 📌 Overview

Streamlit Bank is a full-stack, minimal banking system designed to simulate real-world financial operations such as account creation, transactions, and user management.

The system is built with a strong emphasis on **clean architecture, modular design, and extensibility**, making it a solid foundation for scaling into production-grade financial systems.

---

## 🚀 Features

### Core Functionalities

* Account Creation with Validation (Age ≥ 18, Secure PIN)
* Secure Authentication (Account Number + PIN)
* Deposit & Withdrawal with Constraints
* Balance Tracking
* User Profile Management (Update/Delete)
* Persistent Data Storage

---

## 🧱 Architecture

The system follows a **3-layer architecture**:

```
Presentation Layer:
    - Streamlit Web UI
    - CLI Interface

Application Layer:
    - Bank Class (Business Logic)

Data Layer:
    - JSON-based Storage
```

### Design Principles

* Separation of Concerns
* Single Responsibility Principle
* Reusability via Class Methods
* Stateless UI, Stateful Backend

---

## 🖥️ Interfaces

### 1. CLI Interface

* Interactive terminal-based system
* Useful for debugging and testing core logic

### 2. Web Interface (Streamlit)

* Clean, user-friendly UI
* Sidebar navigation for operations
* Real-time feedback and error handling

---

## 💾 Data Management

* Data is stored in a JSON file (`data.json`)
* Each user record contains:

  ```json
  {
    "name": "",
    "age": "",
    "email": "",
    "pin": "",
    "accountNo.": "",
    "balance": ""
  }
  ```

### Why JSON?

* Lightweight and easy to manage
* No external database dependency
* Ideal for prototyping and small-scale systems

---

## 🔐 Security Considerations

* PIN-based authentication
* Input validation for transactions
* Controlled transaction limits

> ⚠️ Note: PIN is stored in plaintext — in production, hashing (bcrypt) should be used.

---

## ⚙️ Tech Stack

* **Python**
* **Streamlit** (Frontend)
* **JSON** (Storage)
* **Standard Libraries** (random, string, pathlib)

---

## 📈 Scalability Roadmap

This project can be extended into a production-grade system by:

* Replacing JSON with a database (PostgreSQL / MongoDB)
* Adding password hashing (bcrypt)
* Implementing JWT-based authentication
* Introducing REST APIs (FastAPI / Flask)
* Adding transaction history & logs
* Deploying on cloud (AWS / GCP)

---

## 🧪 Example Workflow

1. User creates an account
2. System generates a unique account number
3. User logs in using account number + PIN
4. Performs deposit/withdraw operations
5. Data persists across sessions

---

## 🧠 Engineering Insights

This project demonstrates:

* Full-stack thinking (UI + backend + storage)
* Real-world system modeling (banking operations)
* Transition from CLI → Web application
* Clean abstraction of business logic

---

## 📌 How to Run

### Run Web App

```bash
streamlit run app.py
```

### Run CLI Version

```bash
python main.py
```

---

## 🤝 Contribution

Feel free to fork and extend this project with:

* Database integration
* Authentication improvements
* UI enhancements

---

## 📄 License

MIT License

---

## ⭐ Final Note

This project is a strong demonstration of building **end-to-end systems from scratch**, focusing on correctness, simplicity, and scalability — a mindset aligned with top-tier engineering standards.
