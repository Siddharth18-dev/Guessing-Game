#This Whole Code written in Pycharm IDE and uses Python language for this.

import random
import math
l=int(input("Emter Lower bound:- "))
u=int(input("Enter Upper Bound: "))
x=random.randint(l,u)
print("\n\tYou've only ",round(math.log(u-l+1,2))," chances to guess the integer!\n")
count=0
while count <math.log(u-l+1,2):
    count+=1

    guess=int(input("Guess a number:- "))
    if x==guess:
        print("Congratulations you did it in ",count," try")
        break
    elif x>guess:
        print("You guessed too small!")
    elif x<guess:
        print("You Guessed too high!")
if count >= math.log(u-l+1,2):
    print("\n\tBetter Luck Next time!")
