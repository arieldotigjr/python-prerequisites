# Modules
To import a module, it should be on the same directory where your script is running.

## Syntax
Given that you have a module that has the filename MyModule.py , you can use below syntax to import it on your script
```python
import MyModule
```
If you have a function inside that module and you want to call it
```python
import MyModule
some_operation = MyModule.function_name()
```

```python
#Code snippet for the challenge
numbers_list = [6,1,3,18,12,49,77,54,12]
max_number = max(numbers_list)
print(f'The largest number is {max_number}.')
```
**Note: You do not need to import modules that are already built-in in Python**
