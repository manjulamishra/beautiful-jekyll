---
layout: page
title: Useful Codes
---

## How to create a list of select files from a folder?
There a folder that contains files starting with certain characters. Our task is to make a list of those file. What do we need:
1. Directory path
2. import os

#### Method 1
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



#### Method 2

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



#### Method 3
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


