This is a game Called Rock Paper scissors where you play with computer. You choose a hand choice and Computer randomly chooses its choice and after it is able to challange you.
best of luck 

Code:
import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''


game_images = [rock, paper, scissors]

user_choice = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors. \n"))

if user_choice >= 3 or user_choice < 0:
    print("You typed an Invalid number, You Lose!")
else:   
    print(game_images[user_choice])

    Computer_choice = random.randint(0,2)
    print(f"Computer chose {Computer_choice}")
    print(game_images[Computer_choice])



    if user_choice == 0 and Computer_choice == 2:
        print("You Win!")
    elif Computer_choice ==0 and user_choice == 2:
        print("You lose!")
    elif Computer_choice > user_choice:
        print("You Lose!")
    elif user_choice > Computer_choice:
        print("You Win!")
    elif Computer_choice == user_choice:
        print("It's a draw") 
