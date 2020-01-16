Input file: protein file that records the information of atoms line by line in this protein.
            format(one line): ATOM      1 N    ALA X   1      40.430  32.800  16.670  0.1414 1.6000 0.00290
            input file name: 1X8Q_noW_emSD5000.pqrg
                             where QX8Q represents the protein's name, noW is no water, here means in vaccum environment.
            File storage path: /Users/siwenwang/Desktop/1X8Q_noW_emSD5000.pqrg'
            
Output file: protein file that only records atoms' coordinates, charges and ridius.
            format(one line): 40.430  32.800  16.670  0.1414 1.6000
            where the first three values are x, y, z coordinate respectively, the fouth value is charge value, and the last               one is radius value.
            output file name:1X8Q_noW_emSD5000.pqrg
            File storage path: /Users/siwenwang/Desktop/1X8Q_vacuo.xyzqr
            
        
       
Python code:
'''
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
'''

                      
            
           

            
