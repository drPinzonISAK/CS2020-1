# Unit1: A electronic hardware store

## Criteria A : Planning

### Context of the problem 
There is a hardware store in Karuizawa. This store is quite old, like 1000 years old. The owner, Mr Sakamoito, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application the places the accounting book. Mr.Sakiamoto got a new Mac PC from his nephew, and we would like to use it.


### Justisification of the solution
***Here we will write the design statement: what will do, how, by when***

## Criteria: C :Development

First test of text based menu:

```.py
from datetime import datetime

date = datetime.today()

print('Welcome to Mr.Sakamoto Store Sep 4 10:29 {}'.format(date))
print("What is your name?")
name = input()
print("Hi" + " " + name + "!!")

# create a list of menu
print("This is the menu")
print("=" * 20)

print("1.{}  {}".format("Ram","3$")) 
print("2.{}  {}".format("CPU","5$")) 
print("3.{}  {}".format("Motherboard","5$")) 
print("4.{}  {}".format("GPU","8$"))

print("=" * 20)

print("Which option do you want to get.  ")
options = int(input())

for i in range(3):
  if options == 1 :
    print ("You chose RAM")
    break
  if options == 2 :
    print ("You chose CPU")
    break
  if options == 3 :
    print ("You chose Motherboard")
    break
  if options == 4 :
    print ("You chose GPU")
    break
  else :
    print ("Please chose a number from the list above")
    options =int(input("Which option do you want to get.  "))
```

Warm up activity 

``` py
# This program calculates the sum of even number

sum = 0
for number in range(1000):
  if number%2 ==0 :
    sum += number

print("THe addtion is {}".format(sum))

# Write a program that ask for the first name and last Name
# and create 10 email adresses in the UWCisak domein

import random
print("what is your last name")
lastname = str(input())

print("what is your  first name")
firstname = str(input())

for email in range(10):
  print("{}.{}{}@uwcisak.jp". format(lastname, firstname, random.randint(0,10)))

```
#### Dice simulation

```.py
import random
import matplotlib.pyplot as plt
counts = [0, 0, 0, 0, 0, 0]
num_trial = 2000
for trial in range(num_trial):
  number = random.randint(0,60)
  if number < 9:
    counts[0] += 1
  elif 9 < number < 20:
    counts[1] += 1
  elif 19 < number < 30:
    counts[2] += 1
  elif 29 < number < 40:
    counts[3] += 1
  elif 39 < number < 50:
    counts[4] += 1
  elif 49 < number < 60:
    counts[5] += 1

for index, c in enumerate(counts):
  error = c - num_trial/6
  print("Number of {}s: {},expected {}, error {}".format(index+1, c, num_trial / 6,error))
```
#### Slices

```.py
a = str(input())
print(a[2])   #print the third character of this string
print(a[-2])  #print the second to last character of this string
print(a[:5])  #print the first five characters of this string
print(a[0:-2])#print all but the last two characters of this string
print(a[::2]) #print all the characters of this string with even indices
print(a[1::2])#print all the characters of this string with odd indices
print(a[::-1])#print all the characters of the string in reverse order
print(a[::-2])#print every second character of the string in reverse order, starting from the last one
print(len(a)) #print the length of the given string
```

#### Count to N

It says "This problem is available only for teachers who have a subscription and for their students." :((

#### Series - 1 (using if statement)

```.py
a = int(input("Please input a number "))
b = int(input("Please input a number, but it has to be equal or larger"))

if a <= b:
    for i in range (a, b + 1):
        print(i)
else:
    print("Please keep following conditions above")

```

#### Task for HL

Create a program that asks the user for 10 numbers and then shows those values ordered from smallest to largest.

```.py
num = (input("Please enter 10 numbers ex. 8  3  1  5  6  ... : \n "))

sorted_num = sorted(num.split())
print("This is the list of ordered numbers : \n {}" .format (sorted_num))
```
