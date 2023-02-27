# Jumble_Word_Game

print('welcome to jumble word game!!!!')

import random

word=['secret','python','mean','jupyter','math','probability','number','guess','life']

player=str(input('enter your name : '))

        
score=0      #for scoreing the score
attempt=0       #for scoreing the no. of failed attempts
 
try:
    while True:
    
        theword = word[random.randrange(len(word))]
        theword

        templist = list(theword)
        random.shuffle(templist)
        show_word=''.join(templist)
        show_word
        print("your jumbled word is : ",show_word)
    
        while  attempt<3:
            entered_word = input("enter your guess: ").lower()
            print('You have entered: ' , entered_word)
            pick=random.choice(word)

            if entered_word == theword:
                score += 10
                print("Your Score is :", score)
                print("your guessed word is correct.","you won!!!!!!")
                break
            else:
                print("Wrong guess... try again")
                attempt +=1
                print("Remaining tries",3-attempt)
                continue
        if attempt==3:
            print("limit exceed.....start a new game")

        z = int(input('press 0 to quit and 1 to continue...'))

    
        if z == 0:
            print(player, "Thankyou for playing")
            break
        else:
            attempt = 0
            continue
except:
    print("enter 0 to quit or 1 to continue")
