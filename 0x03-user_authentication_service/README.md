
# Flask Authentication System 🌟  

This project is a **learning exercise** designed to walk you through the creation of a custom authentication system using Flask. While implementing your own authentication system is not recommended in production due to security concerns, this hands-on approach will help you understand the underlying mechanisms. By the end of this project, you'll be able to confidently explain core concepts related to API routes, cookies, form data, and HTTP status codes.

---

## 📚 **Resources**  
Before starting, it’s recommended to go through these resources for better understanding:  
- [Flask Documentation](https://flask.palletsprojects.com/en/latest/)  
- [Requests Module](https://docs.python-requests.org/en/latest/)  
- [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)  

---

## 🎯 **Learning Objectives**  
By completing this project, you will learn to:  
1. Declare API routes in a Flask app.  
2. Retrieve and set cookies.  
3. Handle form data from requests.  
4. Return various HTTP status codes.  

---

## ⚙️ **Requirements**  
To ensure consistency and clarity in your code, please follow these guidelines:  
- **Environment**: Ubuntu 18.04 LTS with Python 3.7  
- **Editor**: Use `vi`, `vim`, or `emacs`  
- **Style**: Follow [pycodestyle](https://pypi.org/project/pycodestyle/) (version 2.5)  
- **Database**: Use SQLAlchemy 1.3.x for ORM operations  
- **Documentation**:  
  - All files, classes, and functions must have meaningful docstrings.  
  - Example:  
    ```python
    """
    This module handles authentication for the Flask app.
    """
    ```  
- **Type Annotations**: Include type hints for all functions.  
- **Executable Files**: Ensure all files are executable (`chmod +x`).  
- **Structure**: The Flask app must only interact with the `Auth` class and never directly with the database.

---

## 🛠️ **Setup**  
1. Install `bcrypt` for password hashing:  
   ```bash
   pip3 install bcrypt
   ```  

2. Clone or set up your project directory and ensure it includes the following:  
   - `README.md`  
   - Python files with proper shebang (`#!/usr/bin/env python3`)  
   - Scripts adhering to the project's file length requirements (use `wc` to check).  

---

## 🧰 **Project Structure**  
The project is organized as follows:  
```
project-directory/  
├── app/  
│   ├── __init__.py   # Flask app setup  
│   ├── auth.py       # Handles authentication logic  
│   ├── models.py     # SQLAlchemy models  
│   ├── routes.py     # API route definitions  
│   └── utils.py      # Helper functions  
├── migrations/       # Database migrations  
├── tests/            # Unit tests  
└── README.md         # Project documentation  
```

---

## 📝 **Key Features**  
### Authentication System 🌐  
1. **User Registration**  
   - Securely hash and store passwords using `bcrypt`.  
2. **User Login**  
   - Verify credentials and manage sessions using cookies.  
3. **Secure API Endpoints**  
   - Protect routes by checking authentication tokens.  

### API Interactions 🚀  
- RESTful API design with proper HTTP methods (`GET`, `POST`, etc.).  
- Detailed status code handling for client and server responses.  

---

## 🧪 **Testing**  
- Use Python's `unittest` framework to test all modules and methods.  
- Run tests with:  
  ```bash
  python3 -m unittest discover tests/
  ```  

---

## 📂 **Example API Usage**  
### **Route**: `/register`  
- **Method**: `POST`  
- **Form Data**:  
  ```json
  {
      "email": "user@example.com",
      "password": "secure_password"
  }
  ```  
- **Response**:  
  ```json
  {
      "message": "User registered successfully."
  }
  ```  

### **Route**: `/login`  
- **Method**: `POST`  
- **Form Data**:  
  ```json
  {
      "email": "user@example.com",
      "password": "secure_password"
  }
  ```  
- **Response**:  
  ```json
  {
      "message": "Login successful.",
      "token": "auth_token_here"
  }
  ```  

---

## 💡 **Tips for Success**  
- Remember: **Never use your custom authentication system in production**! 🛑  
- Always validate user input and handle errors gracefully.  
- Keep your code modular and reusable.  

---

Happy Coding! 🚀
