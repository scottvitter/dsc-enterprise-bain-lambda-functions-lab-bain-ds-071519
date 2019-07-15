
# Lambda Functions - Lab

## Introduction
In this lab, you'll get some hands on practice creating and using lambda functions.


## Objectives

You will be able to:

- Understand what lambda functions are and why they are useful
- Use lambda functions to transform data within lists and DataFrames


## Lambda Functions


```python
import pandas as pd
df = pd.read_csv('Yelp_Reviews.csv')
df.head(2)
```

## Simple Arithmetic

Use a lambda function to create a new column called 'stars_squared' by squarring the stars column.


```python
# Your code here
```

## Dates
Select the month from the date string using a lambda function.


```python
# Your code here
```
# Expected Output

0    11
1    10
2    09
3    02
4    06
Name: date, dtype: object
## What is the average number of words for a yelp review?
Do this with a single line of code!


```python
# Your code here


# Expected Output:  77.06551724137931
```

## Create a new column for the number of words in the review.


```python
# Your code here


df.head(2)
```

## Rewrite the following as a lambda function. Create a new column 'Review_Length'


```python
def rewrite_as_lambda(value):
    if len(value) > 50:
        return 'Short'
    elif len(value) < 80:
        return 'Medium'
    else:
        return 'Long'
#Hint: nest your if, else conditionals
```


```python
# Your code here

df.Review_length.value_counts(normalize=True)
```

## Level Up: Dates Advanced!
<img src="images/date_format_map.png" width="600">  

Overwrite the date column by reordering the month and day from YYYY-MM-DD to DD-MM-YYYY. Try to do this using a lambda function.


```python
df.date.head()
```


```python
# Your code here
```


```python
df.date.head()
```
# Expected Results

0    13-11-2012
1    23-10-2014
2    05-09-2014
3    25-02-2011
4    15-06-2016
Name: date, dtype: object
## Summary

Great! Hopefully you're getting the hang of lambda functions now! It's important not to overuse them - it will often make more sense to define a function so that it's reusable elsewhere. But whenever you need to quickly apply some simple processing to a collection of data you have a new technique that will help you to do just that. It'll also be useful if you're reading someone else's code that happens to use lambdas.
