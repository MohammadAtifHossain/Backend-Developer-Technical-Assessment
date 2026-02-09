![Offshore Staffing Solutions](https://offshorestaffingsolutions.com/wp-content/uploads/2025/03/OSS-768x439.png)

# Problem 2: User Validator
Create a function that checks if user information is valid.

```py
def validate_user(username, email, password):
    """
    Check if user information is valid
    Returns: (is_valid, error_message)
    
    Rules:
    1. Username: 3-10 characters, only letters and numbers
    2. Email: must contain @ and .
    3. Password: at least 6 characters
    """
    
    # TODO: Check username length
    # if len(username) < 3 or len(username) > 10:
    #   return False, "Username must be 3-10 characters"
    
    # TODO: Check username contains only letters and numbers
    # Hint: username.isalnum() might help
    
    # TODO: Check email has @ and .
    
    # TODO: Check password length
    
    # If all checks pass:
    # return True, "User is valid!"
    
    pass

# Test cases
test_cases = [
    ("alice", "alice@example.com", "password123"),  # Should be valid
    ("ab", "alice@example.com", "password123"),     # Username too short
    ("alice!", "alice@example.com", "password123"), # Invalid character
    ("alice", "aliceexample.com", "password123"),   # Email missing @
    ("alice", "alice@example", "password123"),      # Email missing .
    ("alice", "alice@example.com", "12345"),        # Password too short
]

for username, email, password in test_cases:
    is_valid, message = validate_user(username, email, password)
    print(f"User: {username}, Valid: {is_valid}, Message: {message}")
```

**Hint:** Use these string methods:

- len(string) - get length
- string.isalnum() - check if only letters and numbers
- "@" in string - check if contains @
- "." in string - check if contains .

