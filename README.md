# Zuriprojects
Python code for rock paper scissors game
#Game Menu
print()
print ("Play Rock, Paper, Scissors Game!")
print()


#Instruction
print()
print("INSTRUCTIONS")
print("Rock crushes Scissors")
print("Scissors cuts Paper")
print("Paper covers Rock")
print("Use ('R' for 'Rock')")
print("Use ('P' for 'Paper')")
print("Use ('S' for 'Scissors')")
print()

from random import choice
done = False
possible_actions = ["Rock", "Paper", "Scissors"]

user_score = 0
cpu_score = 0

#create game loop
while not done:
    choice_made = None

#create choices
    cpu_input = choice(possible_actions)
    user_input = input("enter R for Rock, P for Paper, S for Scissors. Enter X to Exit:")

    if user_input == "R":
        user_choice = "Rock"
        choice_made = "valid"
    
    elif user_input == "P":
         user_choice = "Paper" 
         choice_made = "valid"

    elif user_input == "S":
         user_choice = "Scissors" 
         choice_made = "valid"
         
    elif user_input == "X":
         user_choice = "Exit" 
    
    else:
        print("Wrong choice. Please read the instructions again!")
    
    if choice_made == "valid":
        print(f"Computer chooses \'{cpu_input}', User chooses \'{user_choice}'")
    
        if user_input == cpu_input:
            print("It's a Tie!:", 'Please enter one : "R", "P", "S":')        
    else:
        if user_input == "R":
           if cpu_input == "S":
            print("Rock smashes scissors! You win!")
        else:
            print("Paper covers rock! You lose.")
    
    if user_input == "P":
        if cpu_input == "R":
            print("Paper covers rock! You win!")
        else:
            print("Scissors cuts paper! You lose.")
    if user_input == "S":
        if cpu_input == "P":
            print("Scissors cuts paper! You win!")
        else:
            print("Rock smashes scissors! You lose.")

    play_again = input('Would you like to play again?(yes/no)')
    if play_again == 'yes':
   
        if choice_made == "Exit":
            print("Thank you for playing")
            print(f"Current Score: Computer = {cpu_score}, User = {user_score}")
            done = True
        
