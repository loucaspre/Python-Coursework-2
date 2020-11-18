# Python-Coursework-2
I. Write a program that reads integer numbers from the user and reports whether each value is positive or negative.
#The loop terminates when the user enters 0 (no message is displayed in this case).
```python
num = int (input("Enter a number: "))
if num > 0:
   print("Positive")
elif num == 0:
   print("") #No specified messaged to be printed/displayed when the user enters number 0. 
else:
   print("Negative")
#END
```
II. Build a program that reads an integer over 100 from the user and displays all of the positive multiples 
#of 7 up to (and including) the value entered by the user. 
#Tip: you can use the range function to build a list of numbers.
```python
#II. Build a program that reads an integer over 100 from the user and displays all of the positive multiples 
#of 7 up to (and including) the value entered by the user. 
#Tip: you can use the range function to build a list of numbers. 

numbers = int (input("Enter a number:")) #Asking the user to enter a number. 
num = range(1, 200) #Creating a list of numbers using the range function. 
list (num)
for n in num: 
    print (n*7) #Diplaying the multiples of seven from my list. 
    if n >= numbers:
        print ("The number above is the result of the value entered &multiplied by 7, That's the end of the program.")
        break
#When the user enters an interger over 100 the last number in the displayed result would be the value entered
#multiplied by 7 in the list 

#If the user attempts to enter a number that is negative or over 200 in the range them the output would just be the
#the range only and it will not stop at the multiplication of the number that was entered by the user.
#END
```
#III. A prime number is an integer greater than one that is only divisible by one and itself. 
#Write a function that determines whether or not its parameter is prime, returning True if it is, 
#and False otherwise. 
#Write a main program that reads an
#integer from the user and displays a message indicating whether or not it is prime. 
```python
#True = Prime and False = Not Prime 

def test_prime(n): #Using the "def" function to create my own function that tests if numbers given are prime or not
#If statements     
    if (n==1):
        return False
    elif (n==2):
        return True;
    else:
        for x in range(2,n):
            if(n % x==0):
                return False
        return True             
print(test_prime(23)) #Please add number in brackets to test if prime or not. 
#END
```
#IV. Saturday nights changed forever when Lotto was introduced back in 1994. Since then, it’s become the nation’s
#favourite game – played by millions in towns and cities across the country. 
#In order to win the top prize in the National
#Lottery’s lotto, one must match all 6 numbers of a ticket to the 6 numbers between 1 and 59 that are drawn by the
#lottery organizer. Write a program that generates a random selection of 6 numbers for a lottery ticket. 
#Ensure that the 6 numbers selected do not contain any duplicates. Finally, display the numbers in ascending order.
```python
import random #importing the random function to generate random integers.

#I'm naming an empty list that will be used to store the 6 numbers in the lottery.
lotteryNumbers = []

#Using the range 0 to 6 in order for the generator to have a 6-number range. 
for i in range (0,6):
  number = random.randint(1,59)
  #In order to avoid duplicates, I am using the while loop:
  while number in lotteryNumbers:
    # if the a number has already been picked, then the programm is required to pick a different number within
    #the same range
    number = random.randint(1,59)
  
  #When the new unique number gets picked, it need to be appended in the list. 
  lotteryNumbers.append(number)

#Sort the list of numbers in ascending order
lotteryNumbers.sort()

#Display the list of numbers on the screen:
print("Today's lottery numbers are: ") 
print(lotteryNumbers)
#END
```
#V. Amusement Park Exercise 

#Amusement park price is based on the age of the guest.
#Guests 3 years of age and less are admitted without charge
#Children between 4 and 11 years of age cost £899.90.
#Seniors over 69 years and over cost £1490.49.
#Admission for all other guests is £1999.99
#Craft a program that begins by reading the ages of all of the guests in a group from the user, with one age entered 
#on each line.The user will enter a blank line to indicate that there are no more guests in the group. 
#Then your program should display the admission cost for the group with an appropriate message. 
#The cost should be displayed using two decimal places.
```python
#Default messages before input
prompt = "What is your age? "
prompt += "\nEnter 'end' when you are finished. "

#Using a while loop followed by if statements in order to relate age with price. 
while True:
    age = input(prompt)
    if age == 'end':
        break
    age = int(age)

    if age <= 3:
        print("Due to your age you are admitted free of charge")
    elif age >= 3 and age <=11:
        print("Your ticket is £899.00")
    elif age >= 69:
        print ("Your ticket is £1490.49")
    else:
        print("Your ticket is £1999.99 dollars")
#For when the prices increase/change depending on age please change print statements to print the appropriate price
#OR change assignment operators IF appropriate. 
#END
