import random

player_score = 0
computer_score = 0

while True:
    player_choice = input("Choose rock, paper, or scissors: ")
    computer_choice = random.choice(["rock", "paper", "scissors"])

    print(f"\nYou chose {player_choice}, and the computer chose {computer_choice}.\n")

    if player_choice == computer_choice:
        print("It's a tie!")
    elif player_choice == "rock":
        if computer_choice == "paper":
            print("You lose!")
            computer_score += 1
        else:
            print("You win!")
            player_score += 1
    elif player_choice == "paper":
        if computer_choice == "scissors":
            print("You lose!")
            computer_score += 1
        else:
            print("You win!")
            player_score += 1
    elif player_choice == "scissors":
        if computer_choice == "rock":
            print("You lose!")
            computer_score += 1
        else:
            print("You win!")
            player_score += 1

    print(f"\nPlayer score: {player_score}")
    print(f"Computer score: {computer_score}\n")

    play_again = input("Do you want to play again? (y/n): ")
    if play_again.lower() != "y":
        break

print("\nThanks for playing!") 
# action-game
