**Day 10: Binary Numbers**

**Task**

Give a base-***10*** integer, ***n***, convert it to binary (base-2). Then find a print the base-***10*** integer denoting the maximum number of consecutive ***1***'s in ***n***'s binary representation.

**Input Format**
A single integer, ***n***.

**Constraints**


$$
1 \leq n \leq 10^{6}
$$


**Output Format**

Print a single base-***10*** integer denoting the maximum number of consecutive ***1***'s in the binary representation of ***n***.

**Sample Input 1**

```
5
```

**Sample Output 1**

```
1
```

**Sample Input 2**

```
13
```

**Sample Output 2**

```
2
```

**Explanation**

Sample Case 1:

The binary representation of **5** is **101**, so the maximum number of consecutive **1**'s is **1**.

Sample Case 2:

The binary representation of **13** is **1101**, so the maximum number of consecutive **1**'s is **2**.

**Code**

```
#!/bin/python3

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    n = int(input().strip())

bin_list = []
while(n > 0):
    div_res = n // 2
    mod_res = n % 2
    bin_list.append(mod_res)
    n = div_res
bin_list = list(reversed(bin_list))

bin_one_num_list = []
temp = []
for i in range(len(bin_list)):
    b = bin_list[i]
    if b == 1:
        temp.append(b)

    if b == 0 or i == len(bin_list) - 1:
        if len(temp) > 0:
            bin_one_num_list.append(len(temp))
        temp = []
print(max(bin_one_num_list))

```



