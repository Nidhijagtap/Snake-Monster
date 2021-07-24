#python code 
def start():
    print("\nYou are standing in a dark room.\nThere is a door to your left and right, which one do you take? (l or r)")
    
    answer = input(">").lower()
    if answer == 'l':
        snake_room()
    else:
        monster_room()

def game_over(reason):
    print(reason+"\nGame over!")
    
def lets_play_again():
    print("\nDo you want to play again?(y or n)")

    answer1 = input(">").lower()
    if  answer1 == 'y':
        start()
    else:
        exit()                 
        
def snake_room():
    print("\nThere is a snake here.")
    print("Behind the Snake is another door.")
    print("The snake is having eggs!")
    print("What would you do? (1 or 2)")
    print("1). Take the eggs.")
    print("2). Taunt the snake.")

    answer2 = input(">").lower()
    if answer2 == '1':
        game_over("\nYou want eggs not teasure !! Thats why the snake killed you.")
        lets_play_again()
    else:
        treasure()
     
def monster_room():
    print("\nNow you entered the room of a monster!")
    print("The monster is sleeping.\nBehind the monster, there is another door. what would you do?(1 or 2)")
    print("1). Go through the door silently.")
    print("2). Kill the monster and show your courage!")

    answer3 = input(">").lower()
    if answer3 == '2':
        game_over("\nThe monster was hungry, he/it ate you")
        lets_play_again()
    else:
        treasure()

def treasure():
    print("\nYou are now in a room filled with diamonds!")
    print("And therre is a door too!")
    print("What would you do?(1 or 2)")
    print("1). Take some diamonds and go through the door.")
    print("2). Just go through the door.")

    answer4 = input(">").lower()
    if answer4 == '1':
        print("Game Over")
    else:
        print("Yay!!! won")
        exit()        

start()
