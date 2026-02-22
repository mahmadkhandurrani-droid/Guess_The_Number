# Guess_The_Number
This repository is a fun game. And A simple command-line game built with Python where the computer randomly selects a number and the player tries to guess it.
import random

def guess_the_number():
    print("=== GUESS THE NUMBER GAME ===")
    print("I have selected a number between 1 and 100.")
    print("Can you guess it?")

    secret_number = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1

            if guess < secret_number:
                print("Too low! Try again.")
            elif guess > secret_number:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You guessed the number in {attempts} attempts.")
                break

        except ValueError:
            print("Please enter a valid number.")

if __name__ == "__main__":
    guess_the_number()
