# password_generator_project
import random
import string

def generate_password(length, use_uppercase, use_numbers, use_symbols):
    character_set = string.ascii_lowercase
    if use_uppercase:
        character_set += string.ascii_uppercase
    if use_numbers:
        character_set += string.digits
    if use_symbols:
        character_set += string.punctuation

    password = ''.join(random.choice(character_set) for _ in range(length))
    return password

# Example usage:
length = 12  # Set the desired length of the password
use_uppercase = True  # Include uppercase letters
use_numbers = True  # Include numbers
use_symbols = True  # Include symbols

password = generate_password(length, use_uppercase, use_numbers, use_symbols)
print(f'Generated Password: {password}')
