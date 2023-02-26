# Requests

`pip install requests`

## Syntax
Sample script to connect to a dummy webservice (https://dummyjson.com/products) and get it's response by using the .get() method of requests library.

```python

import requests
data = requests.get('https://dummyjson.com/products') 

print(data.status_code) # We can check the HTTP status code of the response by using the status_code function, note that we did not used any () on this function because status_code is not callable

data_in_json = data.json()
data_in_text = data.text()
```
