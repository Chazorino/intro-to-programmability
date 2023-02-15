# Variables and Data types
### #1
> :computer: Modify the script below so that it includes your name. You will need to specify a variable called `your_name` and then assign your name to it as a `string`
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

# Getting inputs from the user

Sometimes we want to get input from the user. In python this can be achieved using the build-in `input()` function. 

```python
name = # Add your code here
print("My name is " + name)
```
> :computer: Modify the code to get your name as an input from the user which will then be printed out

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  name = input("What is your name? ")
  print("My name is " + name)
  ```
</details>

# Conditionals

> :computer: Write a script that takes a number from the user and depending on the number returns if the number is less, equal or greater than zero. Be sure to convert the entered number to an integer using the build-in `int()` function


<details>
  <summary>Click here to show solution</summary>
  
  ```python
  number = int(input("Tell me a number! "))
  if number < 0:
    print("Number is less than zero")
  elif number == 0:
    print("Number is exactly zero")
  elif number > 0:
    print("Number is greater than zero")
  ```
</details>

# Functions

## Declaring functions

> :computer: Do it for yourself! Declare a function called `my_first_function` and have it print out the text `I am Anna and this is my first function`. 
> Substitute Anna for your own name.

<details>
  <summary>Click here to show solution</summary>
  
  ```python
  
  def my_first_function():
    print("I am Anna and this is my first function")
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

<div align="right">
   
   [Prev](README.md) - [Next](python_two_tasks.md)
</div>