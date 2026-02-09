![Offshore Staffing Solutions](https://offshorestaffingsolutions.com/wp-content/uploads/2025/03/OSS-768x439.png)

# Problem 1: Simple Chat Logger
Create a class that stores chat messages and can show them.

```py
class ChatLogger:
    def __init__(self):
        # Create an empty list to store messages
        self.messages = []
    
    def add_message(self, username, message):
        """
        Add a message to the log
        Example: add_message("John", "Hello everyone!")
        """
        # TODO: Add the message as a tuple (username, message)
        # Example: self.messages.append(("John", "Hello everyone!"))
        pass
    
    def get_all_messages(self):
        """
        Return all messages
        """
        # TODO: Return the messages list
        pass
    
    def get_messages_by_user(self, username):
        """
        Return only messages from a specific user
        """
        # TODO: Find messages where username matches
        # Hint: Use a for loop to check each message
        pass
    
    def count_messages(self):
        """
        Return how many messages are in the log
        """
        # TODO: Return the length of messages list
        pass

# Test your code
logger = ChatLogger()
logger.add_message("Alice", "Hi there!")
logger.add_message("Bob", "Hello Alice!")
logger.add_message("Alice", "How are you?")

print("All messages:", logger.get_all_messages())
print("Alice's messages:", logger.get_messages_by_user("Alice"))
print("Total messages:", logger.count_messages())
```

```bash
All messages: [('Alice', 'Hi there!'), ('Bob', 'Hello Alice!'), ('Alice', 'How are you?')]
Alice's messages: [('Alice', 'Hi there!'), ('Alice', 'How are you?')]
Total messages: 3
```