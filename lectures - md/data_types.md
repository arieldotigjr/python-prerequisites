# Data types in Python

1. Strings - enclosed by either single quotes (`) or double quotes(")
    ```python
    sample = 'This is a string.'
    ```
2. Numbers
    - integer
    ```python
        a = int(12) #can be created by the keyword int() or Python can infer if you input a whole number
    ```
    - float
    ```python
        b = float(3.1416) #can be created by the keyword float() or Python can infer if you input a number with decimal
    ```
    - fraction
    ```python
    # you will need to import the module fraction
    from fractions import Fraction as frac
        c = frac(3,4)
    ```
    - complex numbers
    ```python
        d = 3 + 4j
    ```
3. Boolean - can only have True or False as value. Defaults to False if the variable does not have any content.

    ```python
    a = True
    b = False
    ```
4. Byte and Byte Arrays
    ```python
    sample = bytearray(15)
    ```
5. Lists - enclosed by brackets ([]), mutable and 0-indexed. Can contain any type of data type as it's element. A data type that is iteratable (sequence)
    ```python
    my_sample_list = ['element',1,[15,2],(4,2,1)]
    #lists are mutable
    my_sample_list[0] = 'new value' #This line will change the index 0 (first) element of the list
    ```

6. Tuples - Unlike list, tuple is immutable (elements are fixed). Enclosed by parentheses. Can also contain any data type as it's element, iteratable (sequence)
    ```python
    my_sample_tuple = (1,2,'string',['list','inside','tuple'])
    #tuples are immutable
    my_sample_tuple[0] = 'new value' # => This will return an error since tuples are immutable and you cannot change the value of its element. You can only append new values using the .append() method
    ```

7. Dictionaries - enclosed by curly brackets {}, **key-value pair**. You can use .get() method to get the value of a key from dictionary
    ```python
    my_sample_dict = {
        'first_name': 'firstname_sample',
        'last_name': 'secondname_sample',
        'suffix':'jr.',
        'email_address': 'example@example.com'
    }
    #to get the value of the first_name from my_sample_dict, you can use below command
    my_sample_dict.get('first_name')
    ```
