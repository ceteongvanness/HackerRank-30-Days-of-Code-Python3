**Day 6: Let's Review**

**Task**
Given a string, ***S***, of length ***N*** that is indexed from ***0*** to ***N - 1***, print its even-indexed and odd-indexed characters as ***2*** space separated string on a single line.

***Note***: **0** is considered to be an even index.

**Input Format**

The first line contains an integer, ***T*** (the number of test cases).

Each line **i** of the T subsequent lines contain a String ***S***.

**Constraints**

***1 <= T <= 10***

***2 <= length of S <= 10000***

**Output Format**

For each String **$$S_{j}$$** (where ***0<= j <= T - 1***), print **$$S_{j}$$**'s even-indexed characters, followed by a space, followed by **$$S_{j}$$**'s  odd-indexed characters.

**Sample Input**

```
2
Hacker
Rank
```

**Sample Output**

```
Hce akr
Rn ak
```

**Code**

```
T = int(input())

if 1 <= T and T <= 10:
    for i in range(T):
        S = input()
        if 2 <= len(S) and len(S) <= 10000:
            print(S[::2], S[1::2])
        else:
            print('Error.')
else:
    print('Error.')
```



