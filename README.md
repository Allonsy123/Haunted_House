# Haunted_House
Haunted House text adventure. 


def Game():

    start = '''
Your friends have dared you to enter your town's famous Haunted Mansion to see
what's inside. AFter much deliberation what DO YOU DO?!?
'''

    print(start)

    hitchhike = "You walk to the road and hitchhike home. THE END."

def end():
    print("Would you like to play again?")
    user_input = input()
    if user_input == "yes":
        return Game()
    elif user_input == "no":

        print("Type 'home' to go back home OR 'Haunted Mansion' to go inside.")
        user_input = input()
        if user_input == "home":
            print("You decide to go back home but you get lost along the way.") # finished the story by writing what happens
            print("Type 'run' to start running OR 'map' to stay in place to find your way home.")
            user_input = input()
            if user_input == "run":
                print("You trip on a rock and become severely injured.")
                print("Type 'stay' to stay where you are OR 'look' seek help.")
                user_input = input()
                if user_input == "stay":
                    print("You're outnumbered by wolves. :( THE END.")
                    return end()
                elif user_input == "look":
                    print("You're injury becomes infected but you make it to the road and are offered a ride to a hospital.")
                    print("Type 'go' to trust them and take their offer OR 'stay' to keep looking for help.")
                    user_input = input()
                    if user_input == "go":
                        print("You make it to the hospital and survive, plus you make a new friend! THE END.")
                        return end()
                    elif user_input == "stay":
                        print("You failed to find help before bleeding to death. :( THE END.")
                        return end()
            elif user_input == "map":
                print("You find your way home safely. THE END.")
                return end()
        elif user_input == "Haunted Mansion":
            print("You choose to go inside but the lights start to flicker.")
            print("Type 'down' to stay downstairs OR 'up' to go upstairs.")
            user_input = input()
            if user_input == "up":
                print("Up you go!")
                print("Type 'bath' to enter the bathroon OR 'bed' to enter the bedroom.")
                user_input = input()
                if user_input == "bath":
                    print("You go into the bathroom.")
                    print("Type 'use' to use the bathroom OR 'leave' to exit it.")
                    user_input = input()
                    if user_input == "use":
                        print("The Mirror shatters and you step on the broken glass. :( THE END.")
                        return end()
                    elif user_input == "leave":
                        print("You leave the bathroom and enter the hallway")
                        print("Type 'exit' to leave the mansion OR 'stay'to wander the halls.")
                        user_input = input()
                        if user_input == "exit":
                            print(hitchhike)
                        elif user_input == "stay":
                            print("Objects start rapidly flying and you become injured. :( THE END")
                            return end()
                elif user_input == "bed":
                    print("You go into the bedroom.")
                    print("Type 'closet' OR 'window' to open them.")
                    user_input = input()
                    if user_input == "closet":
                        print("A skeleton pops out! You panick and start running!")
                        print("Type 'out' to run outside OR 'hall' to run down the hall.")
                        user_input = input()
                        if user_input == "out":
                            print(hitchhike)
                        elif user_input == "hall":
                            print("Objects start rapidly flying and you become injured. :( THE END")
                            return end()
                    elif user_input == "window":
                        print("When the window opened, bats flew in and started flying around the room.")
                        print("Type 'duck' or 'run' to avoid the bats")
                        user_input = input()
                        if user_input == "duck":
                            print("The floor breaks beneath you and you fall. You pass out. :( THE END")
                            return end()
                        elif user_input == "run":
                            print(hitchhike)
            elif user_input == "down":
                print("Fine, you stay down and begin to explore.")
                print("Type 'kitchen' to exit to the kitchen OR 'cemetery' to exit to the cemetery.")
                user_input = input()
                if user_input == "kitchen":
                    print("You slip on cooking oil, fall, and knock yourself unconscious. :( THE END")
                    return end()
                elif user_input == "cemetery":
                    print("As you walk through the cemetery, ghosts start popping out. You decide to run away.")
                    print("Type 'stay' to go back inside the mansion OR 'leave' to continue going home.")
                    user_input = input()
                    if user_input == "stay":
                        print("You get hit by a flying chair and pass out. :( THE END")
                        return end()
                    elif user_input == "leave":
                        print(hitchhike)

Game()
