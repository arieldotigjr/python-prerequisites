# Functions in Python
## Syntax
A `function` in Python can be created by the keyword `def` as shown on below example with parentheses that encloses the input parameters (if needed). It also needs to be terminated by the ***colon(:)*** and the block of codes inside the function needs to be indented.
```python
def greetings():
    print('Good Morning!')
```
You can also create `functions` that have input parameters as shown below.

```python
def my_function(name):
    return ('Hello ' + name + '!. I hope you have an amazing day!.')
my_function('Rj')
```

### Different type of input arguments
1. Arbitrary arguments (*args)

```python
def arb_args(*names):
    print('Hello ' + names[0] + '!')
```

2. Keyword arguments (kwargs)

```python
def kwargs_function(first_name, last_name):
    print(f'Your first name is' first_name + '\n Your last name is ' + last_name)
kwargs_function('Ariel','Dotig')
```

3. Arbitrary Keyword arguments (**kwargs)
```python
def arb_kwargs_func(**user_data):
    print('Your email address is: ' + user_data[email_address])
arb_kwargs_func(first_name = 'Ariel', last_name = 'Dotig', email_address = 'ariel.dotigjr@asurion.com')
```

### Default Parameters

You can create functions that has default values for it's paramaters. This can be shown on the simple script below

```python
def default_params_func(name = 'Joseph'):
    print(name)
#We expect the script to printout The name 'Joseph' unless otherwise the user explicitly assign a different value to it

default_params_funct('David') #We expect this line to print out the name 'David' instead of the default value 'Joseph'

````
