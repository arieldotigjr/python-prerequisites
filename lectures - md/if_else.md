# If statement
## Flowchart
![Flowchart](test-expression.jfif)

## Syntax
In Python, any loop (if, if-else, while, for etc.) should be terminated by the ***colon(:)*** character as shown below.
The block of codes inside the loops should also be indented, this how Python determines which lines of code are part of the loop and which are not.
```python
a = int(input('Enter an integer: '))
b = int(input('Enter another integer: '))
if a>b:
    print(f'{a} is greater than {b}')
```

# If-else statements
## Flowchart
![Flowchart](ifelse.jfif)
## Syntax
Rembember, TERMINATED by the ***colon(:)*** character and ***block of codes inside the loop should be indented.***
```python
#Simple program to print out which user input/ variable is larger.
a=int(input('Enter first variable: '))
b=int(input('Enter second variable: '))
if a>b:
    print(f'{a} is larger than {b}.')
elif a<b:
    print(f'{b} is larger than {a}')
```