#anime suggestion broad recommendations practice random py purposes

import random

print("Welcome to anime suggestions! Please answer the following questions.")

age = int(input("How old are you? "))
gender = input("What is your gender? ")
action = input("Do you like action and battles? (yes/no) ")

if gender not in ["male", "female", "other"]:
    print("ERROR: Please choose a valid gender.") #error handling for invalid arguments in the demographic inputs
    quit()

if action not in ["yes", "no"]:
    print("ERROR: Please choose a valid response for action preference.")
    quit()

if age <= 16 and gender == "male" and action == "yes":
    shounen_anime_gen = random.choice(["Death Note", "Soul Eater", "Assassination Classroom"])
    print(f"You should consider watching {shounen_anime_gen}.")
elif age <= 16 and gender == "female" and action == "no":
    romance_anime_gen = random.choice(["Your Lie in April", "Fruit Baskets", "Clannad"])
    print(f"You should consider watching {romance_anime_gen}.")
elif age >= 16 and action == "yes":
    horror_anime_gen = random.choice(["Another", "Tokyo Ghoul", "Akame ga Kill!"])
    print(f"You should consider watching {horror_anime_gen}.")
else:
    print("Sorry, we couldn't find a suitable anime recommendation based on your preferences, maybe try Avatar or fullmetal?")
