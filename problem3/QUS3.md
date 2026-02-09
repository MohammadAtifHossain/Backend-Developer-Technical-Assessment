![Offshore Staffing Solutions](https://offshorestaffingsolutions.com/wp-content/uploads/2025/03/OSS-768x439.png)

# Problem 3: Simple API
Create a simple web server that handles user messages.

**To Test:**

Run the server: python problem3.py
Open browser: http://localhost:5000/

Test endpoints:
- GET http://localhost:5000/users
- GET http://localhost:5000/users/1
- POST http://localhost:5000/users (curl)

User Info
```bash
users = [
    {"id": 1, "name": "Alice", "email": "alice@example.com"},
    {"id": 2, "name": "Bob", "email": "bob@example.com"}
]
```

You can yous 
- Django REST Framework
- Flask
- FastAPI