# Nested Data Structures

### JSON

### #1

> 💻 Use this JSON data structure and save it as interface.json. Then, write a script that imports the json structure and converts the text-based JSON data into native Python.

> ```python3
> {
>   "ietf-interfaces:interface": {
>     "name": "GigabitEthernet2",
>     "description": "Wide Area Network",
>     "enabled": true,
>     "ietf-ip:ipv4": {
>       "address": [
>         {
>           "ip":"172.16.0.2",
>           "netmask":"255.255.255.0"
>         }
>       ]
>     }
>   }
> }
>
> ```

<details>
  <summary>Click here to show solution</summary>

```python3
import json

file = open('interface.json')

# convert json file to Python dict
data = json.load(file)
print(data)

```

</details>

### #2

💻 From the inported data structure write a code line that can access the 'ip' address.

<details>
  <summary>Click here to show solution</summary>

```python3
import json

file = open('interface.json')

data = json.load(file)
print(data)


ip_address = data["ietf-interfaces:interface"]["ietf-ip:ipv4"]["address"][0]["ip"]
print(ip_address)

```

</details>

## From here you can continue to practice your Python skills by taking on the [Python Exercise](python_three_exercise/Readme.md) or you can move on to REST API Fundamentals by clicking [Next](rest_fundamentals/Readme.md)

<div align="right">

   [Prev](python_two_tasks.md) - [Next](rest_fundamentals/Readme.md)

</div>
