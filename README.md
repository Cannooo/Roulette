# Roulette
Roulette
import random

Money = 1000

print("Roulette")

while 1:
      while Money > 0:
            Ask = input("What colour do you want to put your money on? ")
            AskQty = int(input("How much money do you want to put on? "))

            if Ask == "Black":
                Money = (Money-AskQty)
                b = random.randint(1,36)
                if b >= 16:
                    print("It landed on Black!")
                    Money = (AskQty*2)+Money
                    print(Money)
                else:
                    print("It didn't land on Black!")
                    
                    print(Money)

            elif Ask == "Red":
                Money = (Money-AskQty)
                r = random.randint(1,36)
                if r >= 16:
                    print("It landed on Red!")
                    Money = (AskQty*2)+Money
                    print(Money)
                else:
                    print("It didn't land on Red!")
                    print(Money)

            elif Ask == "Green":
                Money = (Money-AskQty)
                g = random.randint(1,36)
                if g >= 36:
                    print("It landed on Green!")
                    Money = (AskQty*14)+Money
                    print(Money)
                else:
                    print("It didn't land on Green!")
                    print(Money)

                if Money <= 0:
                    Retry = input("Do you want to play again? ")

                    if Retry == "Yes":
                        print("Giving £1000")
                        Money = Money+1000
                    elif Retry == "No":
                        exit
                        
          
else:
    print("")
