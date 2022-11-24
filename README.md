# Word-guessing-Game
for loop

for i   in range (5):
    import random
    name = input("What is your name?")


    print("Good Luck !")

    words = ['rainbow', 'computer','science','programming',
             'python', 'mathematics','player','condition',
             'reverse','water','board','geeks']

    word = random.choice(words)


    print("Guess the charaters")

    guesses = ''

    turns = 5

    points = 50


    while turns > 0:

        failed = 0

        for char in word:

            if char in guesses:
                print(char, end="")

            else:
                print("_")

                failed += 1

        if failed == 0:

            print("  You Win")

            print("The word is:",word)

            print("Your points" , points)
            exit()

        print()
        guess = input("guess a character:")

        guesses += guess

        if guess not in word:

            turns -= 1

            points -= 10

            print("Wrong")

            print("You have", + turns, 'more guesses')

            print("You have", + points, 'points left')

            if turns == 0:
                print("Game Over")
                exit()

            elif points == 0:
                print("You Lose")
                exit()
