### Processing a redundant file in Python to make it become our required data-format 
#### 2. import csv file into Python as a list, in where each element is a dictionary.

 -----
 
 `Description`: This is from the class I took in Udacity called Intro to Data Analysis and Data Wrangling with MongoDB. We will use  `unicodecsv` library or  `csv` library and `DictReader` in these libaries to help us to do the data processing.
 
-----

##### a. Input:

`Input file`: any .csv files

-----          
       
##### c. Python code:

```
import unicodecsv 

enrollments = []
f = open('enrollments.csv','rb')
reader = unicodecsv.DictReader(f)

# here we don't directly use reader since reader is a iterator 
#but we convert reader to a list called enrollment
enrollments = list(reader) 

```

or we can use  `with` statement to write this code:

```
import unicodecsv 

with open('enrollment.csv','rb') as f
  reader = unicodecsv.DictReader(f)
  enrollments = list(reader) 
  

```

We can define the function called parse_csv to do the job:

```
import csv
def parse_csv(datafile):
    data = []
    n = 0
    with open(datafile,'rb') as sd:
        r = csv.DictReader(sd)
        for line in r:
            data.append(line)
    return data 
```
