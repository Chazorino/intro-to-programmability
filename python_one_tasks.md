# Variables and Data types
### #1
> :computer: Modify the script below so that it included your name. You will need to specify a variable called `your_name` and then assign your name to it as a `string`
> 
> ```python3
> # You will need to add code here
> 
> print("Hello " + your_name)
> ```

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  your_name = "Marcel"
  print("Hello " + your_name)
  ```
</details>

### #2
> :computer: Use python to calculate the following operations:
> * Declare a variable `a` with value 10
> * Declare a variable `b` with value 2
> * Declare a variable `c` that is calculated by multiplying `a` and `b`
> * Add 10 to the variable `c`
> * Multiply `c` with itself

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  a = 10
  b = 2
  c = a * b
  c += 10 # alternative: c = c + 10
  c *= c # alternative: c = c * c
  ```
</details>

# Loops and Control Structures

## For loops

### #1
> :computer: Use a for loop to print the text "Good morning!" ten times.

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  for a in range(0, 10):
    print("Good morning!")
  ```
</details>

### #2
> :computer: Modify the code so that it prints 
> 
> ```
> This is the 1. iteration
> This is the 2. iteration
> This is the 3. iteration
> This is the 4. iteration
> This is the 5. iteration
> ```
>
> Pay close attention that you specify the correct range!

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  for a in range(1, 6):
    print("This is the " + str(a) + ". iteration")
  ```
</details>

### #3
> :computer: Lets use this new knowledge to print out all ip addresses that are in a subnet.
> 
> Given a class C Network of `192.168.0.0/24` and a netmask of `255.255.255.0` print out all addresses that are available (including the network and broadcast address)
>
> Remember: The variable of your for loop will be an integer. You will need to cast accordingly!

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  for host_part in range(0, 256):
    ip_address = "192.168.0." + str(host_part)
    print(ip_address)
  ```
</details>

### #4
> :computer: We can use nested for loops to print out multiplication tables. Modify the code below
> 
> ```python
>  for num in range(1, 11):
>       print("Multiplication table for " + str(num))
>       # Use another for loop for the `multiplier` variable 
>       # Insert here
>           res = num ∗ multiplier
>           print(str(num) + ” x ” + str(multiplier) + ” = ” + str(res))
> ```

<details>
  <summary>Click here to show solution</summary>
  
  ```python
    
  for num in range(1, 11):
        print("Multiplication table for " + str(num))
        for multiplier in range(1, 11):
           res = num ∗ multiplier
           print(str(num) + ” x ” + str(multiplier) + ” = ” + str(res))
  ```
</details>

## Control Structures

> :computer: The **FizzBuzz** test is a famous question in entry-level coding interviews. The ask is simple:
> 
> Write a program that prints the numbers from 1 to (including) 20
> 
> * for multiples of three print **Fizz** instead of the number
> * for multiples of five print **Buzz** instead of the number
> * for multiples of both five and three print **FizzBuzz** instead of the number
> * In all other cases print the number
> 
> Three tips: 
> 
> 1) To check if a number is a multiple of another number you can use this conditional:
> 
> ```python
> 
> a = 10
> if a%5 == 0:
>   print("This number is a multiple of 5")
> ```
>
> 2) You can chain multiple conditions with the `and` keyword
> 
> ```python
> 
> age = 17
> if age > 10 and age < 18:
>   print("The person is a teenager")
> ```
> 
> 3) Remember for loops? They might come in handy in this exercise.

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  for num in range(1, 21):
    if num % 3 == 0 and num % 5 == 0:
        print("FizzBuzz")
    elif num % 3 == 0:
        print("Fizz")
    elif num % 5 == 0:
        print("Buzz")
    else:
        print(str(num))
  ```
</details>

# Functions

## Declaring functions

> :computer: Do it for yourself! Declare a function called `my_first_function` and have it print out the text `I am Marcel and this is my first function`. 
> Substitute Marcel for your own name.

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  def my_first_function():
    print("I am Marcel and this is my first function")
  ```
</details>

## Functions with Arguments and Returns

> :computer: Write a function called `test_switch` that receives the `name` and `status` of a switch as a arguments and **returns** either "The switch switch-1 is online" or "The switch switch-1 is offline" depending on wether the status is `active` or `inactive`. The name (`switch-1` in the example) should come from the `name` argument.
> 
> Call the function with the name "switch-2" and the status "inactive". Save the output of that function call in a variable called `out` and print the value of that variable.
> You can use the boilerplate code below as a starting point. You will need to change the questionmarks and fill the body
>
> ```python
> 
> def test_switch(?, ?):
>   
>   return ?
> out = ?
> print(out)
> ```
> 
> Pay close attention to which parts of the program need to be inside the function and which parts need to be outside of the function.

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  def test_switch(name, status):
    if status == "active":
        return "The switch " + str(name) + " is online"
    elif status == "inactive":
        return "The switch " + str(name) + " is offline"

  out = test_switch("switch-2", "inactive")
  print(out)
  ```
</details>

# Advanced Data Structures

## Lists

> :computer: Do it yourself! Create a list that holds the strings one, two, three, four and five. Then append the string six to the list and print the string a **index** 2

<details>
  <summary>Click here to show solution</summary>
  
  ```python3
  l = ["one", "two", "three", "four", "five"]
  l.append("six")
  print(l[2])
  ```
</details>

### Iterating over a list

> :computer: Create a list with the names of three switches: `switch-1`, `switch-2` and `switch-3`. 
> 
> Iterate over the list and print the name of the switches

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  l = ["switch-1", "switch-2", "switch-3"]
  for i in range(0, len(l)):
    print(l[i])
  ```
</details>

### Lists and for-loops revisited

> :computer: You receive a list of switch statuses. The status is a string that is either `active`, `unknown` or `inactive`. 
> 
> Count the number of switches active, unknown or inactive.
> 
> You can use the boilerplate code below:
> 
> ```python
> 
> switch_statuses = ["active", "active", "active", "unknown", "inactive"]
> 
> number_active = 0
> number_unknown = 0
> number_inactive = 0
> 
> # Add your code here!
> print("Number of active switches: " + str(number_active))
> print("Number of unknown switches: " + str(number_unknown))
> print("Number of inactive switches: " + str(number_inactive))
> ```

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  switch_statuses = ["active", "active", "active", "unknown", "inactive"]
  
  number_active = 0
  number_unknown = 0
  number_inactive = 0

  # Add your code here!
  for status in switch_statuses:
    if status == "active":
        number_active += 1
    elif status == "inactive":
        number_inactive += 1
    elif status == "unknown":
        number_unknown += 1

  print("Number of active switches: " + str(number_active))
  print("Number of unknown switches: " + str(number_unknown))
  print("Number of inactive switches: " + str(number_inactive))
  ```
</details>

## Dictionaries

> :computer: Do it for yourself! Declare a `user` dictionary with the keys `first_name`, `last_name` and `age` and then print them all out!

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  user = {}

  user["first_name"] = "Marcel"
  user["last_name"] = "Neidinger"
  user["age"] = 24
  
  print(user["first_name"])
  print(user["last_name"])
  print(user["age"])
  ```

</details>

### Iterating over dictionaries

> :computer: Rewrite the code from the last exercise, the one printing out all the properties of the user dictionary, using the for-each loop and the `keys()` function.
> 
> You can use this boilerplate: 
> 
> ```python
> user = {}
>
> user["first_name"] = "Marcel"
> user["last_name"] = "Neidinger"
> user["age"] = 24
> ```

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  user = {}

  user["first_name"] = "Marcel"
  user["last_name"] = "Neidinger"
  user["age"] = 24
  
  for key in user.keys():
    print(user[key])
  ```

</details>

<div align="right">
   
   [Prev](README.md) - [Next](python_two_tasks.md)
</div>