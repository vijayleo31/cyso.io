import re

def is_safe_input(user_input):
    # Define a pattern for common SQL injection characters
    pattern = re.compile(r"[;\'\"\\/*]")
    if pattern.search(user_input):
        return "Unsafe input detected!"
    return "Input is safe."

print(is_safe_input("SELECT * FROM users;"))
