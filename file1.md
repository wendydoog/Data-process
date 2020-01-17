### Processing a redundant file in Python to make it become our required data-format 
#### 1. Eliminate unnecessary columns in a text file and save it to another file

 -----
 
 `Description`: This is from my Ph.D research area which needs me to convert a .pqrg protein file to a .xyzqr protein file that contains less information by eliminating unnecessary columns.
 
-----

##### a. Input:

`Input file`: protein file that records the information of atoms line by line in this protein.

`format(one line)`: e.g. `ATOM      1 N    ALA X   1      40.430  32.800  16.670  0.1414 1.6000 0.00290`

`input file name`: e.g. `1X8Q_noW_emSD5000.pqrg`

where `1X8Q` represents the protein's name, `noW` is no water, here means in `vaccum` environment.

`File storage path`: e.g. `/Users/siwenwang/Desktop/1X8Q_noW_emSD5000.pqrg'`

-----

##### b. Output:   

`Output file`: protein file that only records atoms' coordinates, charges and ridius.

`format(one line)`: e.g.`40.430  32.800  16.670  0.1414 1.6000`
 
 where the first three values are `x`, `y`, `z` coordinate respectively, the fouth value is `charge value`, and the last               one is `radius value`.

`output file name`:e.g. `1X8Q_noW_emSD5000.pqrg`
            
`File storage path`: e.g. `/Users/siwenwang/Desktop/1X8Q_vacuo.xyzqr`
            
-----      
       
       
##### c. Python code:

```
file1 = open('/Users/siwenwang/Desktop/1X8Q_noW_emSD5000.pqrg', 'r+') 
file2 = open('/Users/siwenwang/Desktop/1X8Q_vacuo.xyzqr', 'a') 
lines = file1.readlines()


for line in lines:
    list = line.split()
    seperator  = ' '
    str =  seperator.join(list[6:11])
    file2.write(str + '\n')

file1.close()
file2.close()
```

