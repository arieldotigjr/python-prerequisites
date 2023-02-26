# For loops
## Flowchart
![]('for-loop-python.jpg')
## Syntax
Like any other Python loops, the line of code that contains the while statement and expression needs to be terminated by the ***colon(:)*** character and the ***block of codes inside the loop should be indented.***
```python

my_list = [1,2,3,4,5]
for nums in my_list:
    if nums>25:
        print(f'The number {nums} is greater than 25.')
        break
    else:
        print(f'The number {nums} is less than 25.')

```
