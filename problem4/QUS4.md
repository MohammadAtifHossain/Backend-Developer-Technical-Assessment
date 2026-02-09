![Offshore Staffing Solutions](https://offshorestaffingsolutions.com/wp-content/uploads/2025/03/OSS-768x439.png)

# Problem 4: Message Search
Create a simple search function for messages.

```py
class MessageSearch:
    def __init__(self):
        # Sample messages for testing
        self.messages = [
            {"id": 1, "user": "Alice", "text": "Hello everyone!", "time": "10:00"},
            {"id": 2, "user": "Bob", "text": "Hi Alice!", "time": "10:01"},
            {"id": 3, "user": "Alice", "text": "How is the weather?", "time": "10:02"},
            {"id": 4, "user": "Charlie", "text": "It's sunny today", "time": "10:03"},
            {"id": 5, "user": "Alice", "text": "That's good news!", "time": "10:04"}
        ]
    
    def search_by_user(self, username):
        """
        Find all messages from a specific user
        """
        results = []
        # TODO: Loop through messages and find matching user
        for msg in self.messages:
            if msg["user"] == username:
                results.append(msg)
        return results
    
    def search_by_keyword(self, keyword):
        """
        Find messages containing a keyword (case-insensitive)
        Example: search for "hello" finds "Hello everyone!"
        """
        results = []
        # TODO: Loop through messages
        # Check if keyword is in message text (convert both to lowercase)
        for msg in self.messages:
            if keyword.lower() in msg["text"].lower():
                results.append(msg)
        return results
    
    def count_messages_by_user(self):
        """
        Count how many messages each user sent
        Return: {"Alice": 3, "Bob": 1, "Charlie": 1}
        """
        counts = {}
        # TODO: Count messages per user
        for msg in self.messages:
            user = msg["user"]
            if user in counts:
                counts[user] += 1
            else:
                counts[user] = 1
        return counts
    
    def add_message(self, user, text):
        """
        Add a new message to the list
        """
        # TODO: Create new message dictionary
        # Give it a new ID (current max ID + 1)
        # Add current time (you can use "now" as placeholder)
        new_id = len(self.messages) + 1
        new_message = {
            "id": new_id,
            "user": user,
            "text": text,
            "time": "now"
        }
        self.messages.append(new_message)
        return new_message

# Test
search = MessageSearch()
print("Alice's messages:", search.search_by_user("Alice"))
print("Messages with 'hello':", search.search_by_keyword("hello"))
print("Message counts:", search.count_messages_by_user())

# Add new message
search.add_message("David", "Good morning!")
print("After adding:", search.count_messages_by_user())
```