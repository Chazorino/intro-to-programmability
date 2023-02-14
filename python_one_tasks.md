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

# Conditionals

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

<div align="right">
   
   [Prev](README.md) - [Next](python_two_tasks.md)
</div>