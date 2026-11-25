# 🛒 E-Commerce Automation Testing

Automated end-to-end test suite for [SauceDemo](https://www.saucedemo.com) — a sample e-commerce web application. Built with **Selenium WebDriver** and **Pytest**, with **Allure** reporting support.

---

## 📋 Test Coverage

| Test File | What It Tests |
|---|---|
| `test_login.py` | Valid user login and redirect to inventory page |
| `test_add_to_cart.py` | Adding a product to cart and verifying the cart badge |
| `test_checkout.py` | Completing the checkout form (name, postal code) |
| `test_e2e_flow.py` | Full purchase flow: login → add to cart → checkout → order confirmation |
| `test_open_site.py` | Site loads correctly |
| `test_sample.py` | Sample arithmetic tests (practice/demo) |

---

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Testing Framework:** Pytest
- **Browser Automation:** Selenium WebDriver
- **Browser:** Google Chrome + ChromeDriver
- **Reporting:** Allure Reports

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/rishil5786/ecommerce_testing.git
cd ecommerce_testing
```

### 2. Create a virtual environment
```bash
python -m venv venv
```

### 3. Activate the virtual environment

**Windows:**
```bash
.\venv\Scripts\activate
```

**Mac/Linux:**
```bash
source venv/bin/activate
```

### 4. Install dependencies
```bash
pip install -r requirements.txt
```

> **Note:** Make sure Google Chrome is installed. ChromeDriver is managed automatically via `webdriver-manager`.

---

## ▶️ Running Tests

**Run all tests:**
```bash
pytest -v
```

**Run a specific test file:**
```bash
pytest test_login.py -v
```

**Run with Allure reporting:**
```bash
pytest -v --alluredir=allure-results
```

---

## 📊 Allure Report

**Generate the report:**
```bash
allure generate allure-results -o allure-report --clean
```

**Open the report in browser:**
```bash
allure open allure-report
```

---

## 📁 Project Structure

```
ecommerce_testing/
│
├── conftest.py           # Shared Pytest fixtures (Chrome WebDriver setup)
├── test_login.py         # Login tests
├── test_add_to_cart.py   # Add to cart tests
├── test_checkout.py      # Checkout flow tests
├── test_e2e_flow.py      # End-to-end purchase flow tests
├── test_open_site.py     # Site availability tests
├── test_sample.py        # Sample/practice tests
├── allure-results/       # Raw Allure test results
└── README.md
```

---

## 🔐 Test Credentials

The project uses the publicly available SauceDemo test credentials:

| Field | Value |
|---|---|
| Username | `standard_user` |
| Password | `secret_sauce` |
| Site | https://www.saucedemo.com |
