---
layout: page
title: Useful Code
---
Python programming snippets on this page are useful working code with examples. I hope to add more code tidbits as a reference for data analysis in terms of data cleaning, manipuation etc. 

### 1. How to create a list of select files from a folder?
There a folder that contains files starting with certain characters. Our task is to make a list of those file. What do we need: 1. Directory path, 2. import os

##### Method 1
using Python built-in 'startswith'


```python
# import os
import os

# directory path
dir_path = "/home/Lab_Project"
file_list = os.listdir(dir_path)

def collect_files(file_list):
    build_file_list = []
    for filename in file_list:
        if filename.startswith("noaa_"): # We want all "noaa_" files
            build_file_list.append(filename)
    return build_file_list
```


```python
dir_path = "/home/Lab_Project"
file_list = os.listdir(dir_path)
collect_files(file_list)
```




    ['noaa_2.csv.1', 'noaa_2.csv']



##### Method 2

Using indexing method:


```python
# import os
import os

# directory path
dir_path = "/home/Lab_Project"
file_list = os.listdir(dir_path)

def collect_files(file_list):
    build_file_list = []
    for filename in file_list:
        if filename[0:5] == 'noaa_': # We want all "noaa_" files
            build_file_list.append(filename)
    return build_file_list
```


```python
dir_path = "/home/Lab_Project"
file_list = os.listdir(dir_path)
collect_files(file_list)
```




    ['noaa_2.csv.1', 'noaa_2.csv']



##### Method 3
Making it more generic to match any string:two input arguments


```python
def collect_files(file_list, str_to_match):
    build_file_list = []
    x = len(str_to_match)
    for filename in file_list:
        if filename[0:x] == str_to_match: 
                    build_file_list.append(filename)
    return build_file_list
```


```python
dir_path = "/home/Lab_Project"
file_list = os.listdir(dir_path)
str_to_match = "Untitled."
collect_files(file_list, str_to_match)
```




    ['Untitled.txt.xlsx',
     'Untitled.txt',
     'Untitled.csv',
     'Untitled.xlsx',
     'Untitled.ipynb']

### 2.How to return middle 3 chars of any odd length string?
Given a string of odd length of 5 or greater, return a string made of the middle three chars of a given String.

```python
def three_middle_chars(any_str):
    if int(len(any_str)%2) ==0:
        print("Error:even length")
    elif len(any_str) < 5:
        print("Error: string length less than 5")
    else:
        middle_str = int(len(any_str)/2)
        return any_str[middle_str-1:middle_str+2]
```
Testing the code:

```python
str_test = "howareyoudoing?" # Example string
```


```python
len(str_test)
```




    15




```python
three_middle_chars(str_test)
```




    'you'



