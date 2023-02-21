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
**Note: You do not need to import modules that are already built-in in Python**