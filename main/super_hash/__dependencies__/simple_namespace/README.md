# What is this?

This is a very simple python tool for creating namespaces. It tries to solve the problem that there is [no elegant way to create singleton classes](https://stackoverflow.com/questions/31875/is-there-a-simple-elegant-way-to-define-singletons) or nested namespaces in python.

# How do I use this?

`pip install simple_namespace`

```python
from simple_namespace import namespace

@namespace
def MyNamespace():
    my_value = 10
    def my_function(arg1):
        return 99
    
    return locals()

# prints 10
print(MyNamespace.my_value) 
```