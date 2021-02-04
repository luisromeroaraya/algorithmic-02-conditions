# Conditions
* Type of challenge: **learning**
* Duration: **60 min**
* Team challenge: **solo**

## Learning objectives
At the end of this challenge you should:
* understand the concept of conditions
* be able to write conditions

## The mission
This challenge will have you play around with the concept of [conditions](https://en.wikipedia.org/wiki/Conditional_(computer_programming)), complete the exercises down below after you’ve read the explanations.

With the help of conditions you can execute parts of code if requirements are met. It allows you to create program with different outcome depending on the input.

A useful predefined function would be one returning random numbers. Well here you go, **random** does just that and all languages have an equivalent.

Example
``` 
// This algorithm will output "Yes, I am John Doe."
constant NAME = "John Doe"
if ($NAME == "John Doe") then {
	output("Yes, I am $NAME.")
} else {
	output("No, I am not $NAME.")
}

// The algorithm will output a number between 0 and 100.
integer nbr = random(100)
output($nbr) // Prints a random numbers between 0 and 100
```

## Exercises
Instructions
* write your algorithm on paper
* detail each and every step
* indicates the types of used variables

*I will be using [Python3](https://repl.it/languages/python3) to write and test the algorithms*

I - cinema tariffs
- [x] In a cinema the full tariff is 10 €, the reduced one is 8 €. Write an algorithm which given a boolean indicating if the person can have a reduced tariff prints the price to pay.

```
reduced=input("Can you have a reduced tariff? (y/n):")
if reduced=="y":
    reduced=True
else:
    reduced=False

if reduced:
    print("Price to pay: 8€")
else:
    print("Price to pay: 10€")
```

II - maximum
- [x] Write an algorithm which given 3 numbers finds the maximum.

```
number1=int(input("Enter your first number:"))
number2=int(input("Enter your second number:"))
number3=int(input("Enter your third number:"))

if number1 >= number2:
    maximum=number1
else:
    maximum=number2

if number3 >= maximum:
    maximum=number3

print("The maximum number is:",maximum)
```

III - identical dice
- [x] Write an algorithm which throws 3 dices and finds out the number of identical value, three, two or none.

```
import random
dice1=random.randint(1,6)
dice2=random.randint(1,6)
dice3=random.randint(1,6)
identical=0

if dice1 == dice3 or dice1 == dice2 or dice2 == dice3:
    identical=identical+2

if dice1 == dice2 and dice2 == dice3 :
    identical=identical+1

print("The dices were thrown.","Dice 1 =",dice1,",","Dice 2 =",dice2,",","Dice 3 =",dice3,".")
print("Number of identical value:", identical)
```

IV - day’s number
- [x] Write an algorithm which given the number of a day returns its name.

```
number=int(input("Please enter the number of a day (1-7):"))
if number == 1:
    day="Monday"
elif number == 2:
    day="Tuesday"
elif number == 3:
    day="Wednesday"
elif number == 4:
    day="Thursday"
elif number == 5:
    day="Friday"
elif number == 6:
    day="Saturday"
elif number == 7:
    day="Sunday"
else:
    day="That is not a valid number"

print("The name of that day is:",day)
```

V - print shop
- [x] A print shop charges 0.12 € the ten first copy, 0.11 € the next 20 and 0.10 € from there. Write an algorithm which given a number of copies and calculates the price.

```
copies=int(input("Please enter number of copies:"))
ten=10
twenty=0
rest=0

if copies <= 10:
    ten=copies
elif copies <= 30:
    twenty=copies-10
else:
    twenty=20
    rest=copies-30

price=float((ten*0.12)+(twenty*0.11)+(rest*0.10))
print("Copies at 0.12€:", ten, ".", "Copies at 0.11€:", twenty, ".", "Copies at 0.10€:", rest, ".")
print("Your total price is:", round(price,2),"€")
```

## Resources
* [conventions](https://github.com/becodeorg/BXL-Swartz-4-27/blob/master/1.The-Field/7.Algorithmic/conventions.adoc)
* [conditions](https://computersciencewiki.org/index.php/Conditionals)
