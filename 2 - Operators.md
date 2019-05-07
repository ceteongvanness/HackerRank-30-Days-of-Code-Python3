**Day 2 : Operators**

**Task**

Given the meal price (base cost of a meal), tip percent (the percentage of the mean price being added as tip), and tax percent (the percentage of the meal price being added as tax) for a meal, find and print the meal's total cost.

**Note:** be sure to use precise values for your calculations, or you may end up with an incorrectly rounded result!

**Input Format**

There are **3** lines of numeric input:

The first line has a double, ***mealCost*** (the cost of the meal before tax and tip).

The second line has an integer, ***tipPercent*** (the percentage of mealCost being added as tip).

The third line has an integer, ***tax Percent*** (the percentage of mealCost being added as tax).

**Output Format**

Print the total meal cost, where ***totalCost*** is rounded integer result of the entire bill(***mealCost*** with added tax and tip.)

**Sample Input**

```
12.00
20
8
```

**Sample Output**

```
15
```

**Explanation**

Given:

$$
\text {mealCost} =12, \text { tipPercent }=20, \text { taxPercent }=8
$$

Calculations:

$$
t i p=12 \times \frac{20}{100}=2.4
$$

$$
\operatorname{tax}=12 \times \frac{8}{100}=0.96
$$

$$
totalCost =\text {mealCost}+t i p+t a x=12+2.4+0.96=15.36
$$

$$
round(\ { totalCost })=15
$$

We round ***totalCost*** to the nearest dollar (integer) and then print our result,***15***.

**Code**

```
import sys

# Complete the solve function below.
if __name__ == '__main__':
	meal_cost = float(input())
	tip_percent = int(input())
	tax_percent = int(input().strip())
	
	tip_amount = meal_cost * tip_percent / 100
	tax_amount = meal_cost * tax_percent / 100
	total_cost = round(meal_cost + tip_amount + tax_amount)
	
	print(str(total_cost))
```



