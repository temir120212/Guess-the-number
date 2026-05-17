# Guess-the-number
A simple console-based "Guess the Number" game written in Python.

```python
import random

secret_number = random.randint(1, 100)
attempts = 0
number_limit = 100

print(f"I've guessed a number from 1 to {number_limit}. Try to guess it!")

while True:
    guess = int(input("Enter your number: "))
    
    if guess > number_limit:
        print(f"Error! The number exceeds the limit (up to {number_limit})")
        continue
        
    attempts += 1

    if guess < secret_number:
        print("The guessed number is higher!")
    elif guess > secret_number:
        print("The guessed number is lower!")
    else:
        print(f"Congratulations! You guessed it in {attempts} attempt(s)!")
        break
