# Math-with-Python-assessment-week-1
Try writing an “even-odd vending machine,” which will take a number as input and do two things:

Print whether the number is even or odd.
Display the number followed by the next 9 even or odd numbers.
If the input is 2, the program should print even and then print 2, 4, 6,
8, 10, 12, 14, 16, 18, 20. Similarly, if the input is 1, the program should print odd and then print 1, 3, 5, 7, 9, 11, 13, 15, 17, 19.
Your program should use the is_integer() method to display an error message if the input is a number with significant digits beyond the decimal point.

def even_odd(num):
if num % 2 == 0:
print("even")
else:
print("odd")
for i in range(0, 20, 2):
print(num + i)

def even_odd_unnecessary(num):
 Same function as even_odd but with unnecessary print() formatting just
because
if num % 2 == 0:
print("even")
else:
print("odd")
for i in range(0, 18, 2):
print(num + i, sep='', end=', ', flush=True)
print(num + 18, sep='', end='.\n', flush=False)

if name == 'main':
even_odd(2)

even_odd_unnecessary(2)
even_odd_unnecessary(9)
Chapter 2.  Programming Challenge 2 page 55, Exploring a Quadratic Function Visually

Quadratic function calculator
'''

Assume values of x ux_values = [-1, 1, 2, 3, 4, 5] vfor x in x_values:

             # Calculate the value of the quadratic function
             y = x**2 + 2*x + 1
             print('x={0} y={1}'.format(x, y))
             
             
Chapter 3.  Programming Challenge 2 page 89, Statistics Calculator

Statistics Calculator

Implement a statistics calculator that takes a list of numbers in the file mydata.txt and then calculates and prints their mean, median, mode, variance, and standard deviation using the functions we wrote earlier in this chapter.

importing the module

import pandas as pd

creating a series

s = pd.Series(data = [5, 9, 8, 5, 7, 8, 1, 2, 3,

                  4, 5, 6, 7, 8, 9, 5, 3]) 
displaying the series

print(s)

Finding the mean of the series using the mean() function.

finding the mean

print(s.mean())

Finding the standard deviation of the series using the std() function.

finding the Standard deviation

print(s.std())

Example 2 : Finding the mean and Standard Deviation of a Pandas DataFrame.

importing the module

import pandas as pd

creating a dataframe

df = pd.DataFrame({'ID':[114, 345, 157788, 5626],

               'Product':['shirt', 'trousers', 'tie', 'belt'], 

               'Color':['White', 'Black', 'Red', 'Brown'], 

               'Discount':[10, 10, 10, 10]}) 
displaying the DataFrame

print(df)

Finding the mean of the DataFrame using the mean() function.

finding the mean

print(df.mean())

Finding the standard deviation of the DataFrame using the std() function.

finding the Standard deviation

print(df.std())

Chapter 4.  Programming Challenge 4 page 117, Solving Single-Variable Inequalities

from sympy.abc import x
from sympy import solve_rational_inequalities, Poly

solve_rational_inequalities([[
((Poly(-x + 1), Poly(1, x)), '>='),
((Poly(-x + 1), Poly(1, x)), '<=')]])

solve_rational_inequalities([[
((Poly(x), Poly(1, x)), '!='),
((Poly(-x + 1), Poly(1, x)), '>=')]])
