import random

def guess_the_number():
    number_to_guess = random.randint(5000, 10,000)
    attempts = 0
    guessed = False

    print("Welcome to 'Guess the Number'!")
    print("I'm thinking of a number between 5000 and 10,000.")

    while not guessed:
        try:
            user_guess = int(input("Enter your guess: "))
            attempts += 1
            
            if user_guess < number_to_guess:
                print("Too low! Try again.")
            elif user_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                guessed = True
                print(f"Congratulations! You've guessed the number {number_to_guess} in {attempts} attempts.")
        except ValueError:
            print("Please enter a valid number.")

guess_the_number()
