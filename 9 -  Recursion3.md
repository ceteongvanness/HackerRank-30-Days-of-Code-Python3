**Day 9: Recursion 3**

**Recursive Method for Calculating Factorial**
$$
(N)=\left\{\begin{array}{ll}{1} & {N \leq 1} \\ {N \times \text { factorial }(N-1)} & {\text { otherwise }}\end{array}\right.
$$
**Task**

Write a factorial function that takes a positive integer, ***N*** as parameter and prints the result of ***N!***(***N*** factorial).

**Note**: If you fail use recursion or fail to a name your recursive function factorial or Factorial, you will get a score of ***0***.

**Input Format**

A single integer, ***N*** (the argument to pass to factorial)

**Constraints**
$$
2 \leq N \leq 12
$$
Your submission must contain a recursive function named factorial.

**Output Format**
Print a single integer denoting **N!**.

**Sample Input**

```
3
```

**Sample Output**

```
6
```

**Explanation**

Consider the following steps:

1. ***factorial (3) = 3 x factorial(2)***
2. ***factorial (2) = 2 x factorial(1)***
3. ***factorial (1) = 1***

From step **2** and **3**, we can say ***factorial(2) = 2 x 1 = 2***; then when we apply the value from ***factorial(2)*** to step **1**, we get ***factorial(3) = 3 x 2 x 1 = 6***. Thus, we print ***6*** as our answer.

**Code**

```
#!/bin/python3

import math
import os
import random
import re
import sys

# Complete the factorial function below.
def factorial(n):

    if n <= 1:
        return 1
    else:
        return n * factorial(n-1)

if __name__ == '__main__':
    n = factorial(int(input()))

print(n)
```

