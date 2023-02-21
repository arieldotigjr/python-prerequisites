# Libraries
Similar to module, you can use libraries by using the statement `import` however, you need to install the library first using `pip`. To install a library, use the command `pip install <library name>` on your command prompt.
## Syntax
- If we want to import the library requests, then we need to use below line of code
    ```python
    import requests
    ```

- We can also rename the library when importing as shown below
    ```python
    import pandas as pd
    ```

- To use a function inside a library
    ```python
    import library_name
    some_data = library_name.function_name(input_parameters)
    ```