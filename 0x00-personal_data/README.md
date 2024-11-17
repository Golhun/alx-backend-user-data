
# PII Data Management and Authentication Project 🔒

## Overview 📋

This project focuses on **managing Personally Identifiable Information (PII)** securely and ensuring **robust authentication mechanisms** using Python. It involves building functionalities for obfuscating sensitive information in logs, encrypting passwords, and securely authenticating to databases. By adhering to best practices, this project demonstrates a strong understanding of data protection and application security.

---

## Features 🌟

1. **PII Management**:
   - Examples and identification of PII fields.
   - Implementation of a log filter to obfuscate sensitive PII fields.

2. **Password Encryption**:
   - Secure password hashing using the `bcrypt` package.
   - Validation of user-provided passwords against stored hashed passwords.

3. **Secure Authentication**:
   - Database authentication using environment variables for sensitive credentials.

4. **Logging Mechanisms**:
   - Configurable log levels and output formatting.
   - Logging sensitive data with PII obfuscation to maintain compliance.

---

## Learning Objectives 🎯

By the end of this project, you will be able to:
- Identify **PII** and differentiate between PII, non-PII, and personal data.
- Implement **log filters** that obfuscate sensitive PII fields.
- **Hash passwords** securely and validate input against hashed passwords.
- Authenticate to a database using **environment variables** for sensitive credentials.

---

## Installation and Setup 🛠️

### Prerequisites
- **Ubuntu 18.04 LTS**.
- **Python 3.7** installed and configured.
- Required Python packages:
  - `bcrypt`
  - `logging`

### Setup
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <project_directory>
   ```

2. Install dependencies:
   ```bash
   pip install bcrypt
   ```

3. Configure environment variables for database authentication:
   ```bash
   export DB_USERNAME=<your_db_username>
   export DB_PASSWORD=<your_db_password>
   ```

---

## Usage 🚀

### Obfuscating PII in Logs
Run the script to filter and log messages with sensitive data:
```bash
python obfuscate_pii.py
```

### Password Encryption
Hash a password:
```python
from encrypt import hash_password

hashed = hash_password("my_secure_password")
print(hashed)
```

Validate an input password:
```python
from encrypt import is_valid_password

is_valid = is_valid_password("my_secure_password", hashed)
print(is_valid)  # True or False
```

### Secure Database Authentication
Ensure that your environment variables for `DB_USERNAME` and `DB_PASSWORD` are set. Use the database connection module to securely authenticate.

---

## Key Concepts 📚

### Personally Identifiable Information (PII)
Examples of PII include:
- Full Name
- Email Address
- Phone Number
- Social Security Number (SSN)
- Credit Card Details

### Log Filtering
- Obfuscate sensitive fields (e.g., replace credit card numbers with `****`).
- Ensure logs are still useful for debugging without exposing sensitive data.

### Password Encryption
- Use **bcrypt** to hash and verify passwords.
- Store only the hashed passwords, not the plaintext versions.

### Secure Authentication
- Use environment variables to protect sensitive credentials.
- Avoid hardcoding usernames and passwords in the source code.

---

## Example Logs 📋

### Input
```text
{"name": "John Doe", "email": "johndoe@example.com", "credit_card": "1234-5678-9876-5432"}
```

### Output
```text
{"name": "John Doe", "email": "johndoe@example.com", "credit_card": "****-****-****-5432"}
```

---

## Testing 🧪

Unit tests are available in the `tests` directory. To run all tests:
```bash
python -m unittest discover tests/
```

---

Enjoy coding securely! 🔐
