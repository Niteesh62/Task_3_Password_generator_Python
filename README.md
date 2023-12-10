# Task_3_Password_generator_Python
import random
import string

def generate_password(length=12, include_digits=True, include_special_chars=True):
    
    # Define character sets
    
    letters = string.ascii_letters
    digits = string.digits if include_digits else ''
    special_chars = string.punctuation if include_special_chars else ''

    # Combine character sets
    all_chars = letters + digits + special_chars

    # Ensure the password length is at least 4 characters
    length = max(4, length)

    # Generate password
    password = ''.join(random.choice(all_chars) for _ in range(length))
    
    return password

# Example usage:
password = generate_password()
print("Generated Password:", password)
