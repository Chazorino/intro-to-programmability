# Data Structures

## Lists

> 💻 Create a list that holds the strings one, two, three, four and five. Then append the string six to the list and print the string a **index** 2

<details>
  <summary>Click here to show solution</summary>

```python
  l = ["one", "two", "three", "four", "five"]
  l.append("six")
  print(l[2])
```
</details>

## Dictionaries

> 💻 Declare a `user` dictionary with the keys `first_name`, `last_name` and `age` and then print them all out!

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

# Loops 

### #1

> 💻 Use a for loop to print the text "Good morning!" ten times.

<details>
  <summary>Click here to show solution</summary>

```python
  
  for a in range(0, 10):
    print("Good morning!")
```
</details>

### #2

> 💻 Modify the code so that it prints
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

> 💻 Lets use this new knowledge to print out all ip addresses that are in a subnet.
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

> 💻 We can use nested for loops to print out multiplication tables. Modify the code below
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

# Data Structures and Loops

## Iterating over a list

> 💻 Create a list with the names of three switches: `switch-1`, `switch-2` and `switch-3`.
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

## Lists and for-loops

> 💻 You receive a list of switch statuses. The status is a string that is either `active`, `unknown` or `inactive`.
>
> Count the number of switches active, unknown or inactive.
>
> You can use the boilerplate code below:
>
> ```python‚
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

## Iterating over dictionaries

> 💻 Rewrite the code from the last exercise, the one printing out all the properties of the user dictionary, using the for-each loop and the `keys()` function.
>
> You can use this boilerplate:
>
> ```python
> user = {}
>
> user["first_name"] = "Frederic"
> user["last_name"] = "Wagner"
> user["age"] = 28
> ```

<details>
  <summary>Click here to show solution</summary>

```python
  
  user = {}

  user["first_name"] = "Frederic"
  user["last_name"] = "Wagner"
  user["age"] = 28
  
  for key in user.keys():
    print(user[key])
```

</details>




<div align="right">

   [Prev](python_one_tasks.md) - [Next](python_two_json.md)
</div>