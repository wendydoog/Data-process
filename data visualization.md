#### Line plot or reg plot

1. libraries:
```
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
```

2. main code:
```
fig = plt.figure(figsize = (5,4))

#line1 = sns.lineplot(x = numpy_array1,y = numpy_array2, marker = 'o',label='line1')
#line1.lines[0].set_linestyle("--")
#line.axhline(0, ls='--',color ='r')
sns.regplot(x = atom_num, y = dif)

#plt.grid(True)
plt.xlabel('x label',fontsize=13)
plt.xticks(fontsize = 13)
plt.ylabel('y label',fontsize=13)
plt.yticks(fontsize = 13)

#plt.legend( loc='lower right',fontsize=13)
#fig.legend( bbox_to_anchor=(0.43, -0.16, 0.5, 0.5),fontsize=13)


fig.savefig('file_name.pdf',bbox_inches='tight')

```

3. inputs:

In above code, x and y are numpy array. The reason to use numpy array is to do linear calculation easily. 
