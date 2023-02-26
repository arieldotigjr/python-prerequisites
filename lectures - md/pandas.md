# Pandas

`pip install pandas`

## Creating a dataframe

Column names are `first_name`, `last_name`, `student_grade` and `id_number` as the index of the dataframe.

1. From lists

In this approach, we need to ensure that all of our lists that we'll transfer to the dataframe has the same lenght or else the Python interpreter will return a `ValueError: Length of values (<length of list>) does not match length of index`

```python
import pandas as pd

#First, create an empty dataframe
df = pd.DataFrame()
fname = ['Piolo','Jericho','Bea','Sherlock','James'] #Create a list for the first name
lname = ['Pascual','Rosales','Alonzo','Holmes','Reid'] #Create a list for the second name
student_grade = [95,95,95,100,95] #create a list for the grades
id_number = [81341,31678,33135,32135,94831] #Create a list for the id number
#Assign each list to the columns
df['first_name'] = fname
df['last_name'] = lname
df['student_grade'] = student_grade
df['id_number'] = id_number
#Use the id_number as index. the parameter inplace=True means that we will overwrite the dataframe 'df' with the new value with id_number as index
df.set_index('id_number',inplace=True)
```

2. From JSON/ dictionary

```python
import pandas as pd
# Build the dictionary, the key will be the column, while the values will be the values of each column (list)

student_data = {
    'first_name':['Piolo','Jericho','Bea','Sherlock','James'],
    'last_name': ['Pascual','Rosales','Alonzo','Holmes','Reid'],
    'student_grade':[95,95,95,100,95],
    'student_id': [81341,31678,33135,32135,94831]
}

#Create the dataframe with your json or dictionary as data
df = pd.DataFrame(student_data)
df.set_index('student_id',inplace=True)

```
