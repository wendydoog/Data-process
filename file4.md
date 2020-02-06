### Processing a redundant file in Python to make it become our required data-format 
#### 2. Read excel file into Python as a list, in where each element is a list.

 -----
 
 `Description`: This is from the class I took in Udacity called Data Wrangling with MongoDB. We will use  `xlrd` module to help us to do the data processing. `Zipfile` can help ua open a zipped file.
 
-----

##### a. Input:

`Input file`: any .xlsx or .xls files

-----          
       
##### b. Python code:

```
import xlrd
from zipfile import Zipfile
datadile  = 'filename.xls'

def open_zip(datafile):
    with Zipfile('{0}.zip'.format(datafile,'r')) as myzip:
        myzip.extractall()
        
def parse_file(datafile):
    workbook = xlrd.open_workbook(datafile)
    sheet = workbook.sheet_by_index(0)
    sheet_data = [[sheet.cell_value(r,col)
                     for col in range(sheet.ncols)]
                         for r in range(sheet.nrows)]
    return sheet_data



```


