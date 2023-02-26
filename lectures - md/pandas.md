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
3. You can also use csv or excel files as a data source for your dataframe using the read_csv() and read_excel() functions.
```python
df_excel = pd.read_excel(filename,engine='openpyxl')
df_csv = pd.read_csv(filename)
```

## Using the iterrows() function

`iterrows()` is a built-in function in pandas. It can be used to iterate all throughout your dataframe and perform operations on a row-level. We use .iterrows() in a for loop since it generates an iterator object of the dataframe and return the index and row values of the dataframe.

```python
import pandas as pd
student_data = {
    'first_name':['Piolo','Jericho','Bea','Sherlock','James'],
    'last_name': ['Pascual','Rosales','Alonzo','Holmes','Reid'],
    'student_grade':[95,95,95,100,95],
    'student_id': [81341,31678,33135,32135,94831]
}
df = pd.dataframe(student_data)

for index,row in df.iterrows():
    print(f'The student {row["last_name"], row["first_name"]} has a grade of {row["student_grade"]}') #In this line, we get the current value of the rows with column last_name, first_name and student_grade.

```

## Using the .query() function

The query() function is used to filter out data from your dataframe based the conditions/ filters you've set. It returns a new dataframe with the data that conforms to your filters. You can use the column names and conditional operators to create filters.

```python
import pandas as pd

incident_data = pd.read_csv(incident_from_snow,index='number')
incident_data.query('short_description.str.contains("JPK")', engine='python') #This part, I just researched from stack overflow :D, we can use this to search for a specific string from the value of the columns as filter
```
