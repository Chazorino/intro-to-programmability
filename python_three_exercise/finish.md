# That's It!

Congratulations! You wrote your first little application in python.

To repeditively test your python script, remove the ```interface()```line and append the main block at the end of the `main.py` file. Your file should have the following structure:

```python3
def createItem():
    ## code block omitted

def listItems():
    ## code block omitted

def markItemDone():
    ## code block omitted

def interface():
    ## code block omitted

# remove this line
# interface() 

def main():
    while True:
        interface()

if __name__ == "__main__":
    main() 
```

Now, you can run your main.py python app.

Feel free to expand on this example. Functionality you could add includes

* Checking that the id really does not exist when creating a new todo item
* Providing a function to update a existing todo item
* Allow different types of fields
* Check that a todo item with a provided id actually exists when deleting a item

<div align="right">

   [Prev](done.md)

</div>
