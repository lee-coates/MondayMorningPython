# 10 Interesting Facts About Python
The scripts in this folder are based on the GeeksForGeeks article written by Harshit Gupta. The original article can be found at https://www.geeksforgeeks.org/py-facts-10-interesting-facts-about-python/. This repo is an educational reproduction of this article for training purposes.

## Script 1 - The Zen of Python
Python is beloved by its developers. Try the following code in the python interpreter for a perfect example:
```
import this
```
### Script 1 - Output
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!

## Script 2 - Multiple Return Values
Python is praised for its brevity. For example, Python handles multiple return values, greatly reducing lines of code:
```
def func(): 
   return 1, 2, 3, 4, 5
  
one, two, three, four, five = func() 
  
print(one, two, three, four, five)
```

## Script 3 - Else in a For Loop
In its [Pythonic](https://stackoverflow.com/questions/25011078/what-does-pythonic-mean) way, even for loops are reconsidered, in this case adding an optional else clause:
```
def func(array): 
     for num in array: 
        if num%2==0: 
            print(num) 
            break # Case1: Break is called, so 'else' wouldn't be executed. 
     else: # Case 2: 'else' executed since break is not called 
        print("No call for Break. Else is executed")  
  
print("1st Case:") 
a = [2] 
func(a) 
print("2nd Case:") 
a = [1] 
func(a)
```

## Script 4 - All Reference, No Pointers
The GeeksForGeeks article points out an important distinction--In Python, everything is done by reference. For a deeper understanding on what this means, I'd *reference* this amazing [StackOverflow Discussion](https://stackoverflow.com/questions/373419/whats-the-difference-between-passing-by-reference-vs-passing-by-value).

## Script 5 - Function Argument Unpacking
For many Pythonistas, one of the main benefits of working with Python is how it handles collections like Lists and Dictionaries. A quick example is unpacking, also known as the Splat operator:
```
def point(x, y): 
    print(x,y) 
  
foo_list = (3, 4) 
bar_dict = {'y': 3, 'x': 2} 
  
point(*foo_list) # Unpacking Lists 
point(**bar_dict) # Unpacking Dictionaries 
```

## Script 6 - Enumerate
Enumeration is the concept of going through a collection of items one by one. Python can do that:
```
# Know the index faster 
vowels=['a','e','i','o','u'] 
for i, letter in enumerate(vowels): 
    print (i, letter) 
```

## Script 7 - Chaining Comparison Operators
Python is written to be very readable, even when speaking in the language of mathematics. Take comparison operators for example--Humans commonly chain these operations, so why not in our programs too!
```
# Chaining Comparison Operators 
i = 5; 
  
ans = 1 < i < 10
print(ans) 
  
ans = 10 > i <= 9
print(ans) 
  
ans = 5 == i 
print(ans) 
```

## Script 8 - Python "Knows" Infinity
Speaking of handles Mathematics...
```
# Positive Infinity 
p_infinity = float('Inf') 
  
if 99999999999999 > p_infinity: 
    print("The number is greater than Infinity!") 
else: 
    print("Infinity is greatest") 
  
# Negetive Infinity 
n_infinity = float('-Inf') 
if -99999999999999 < n_infinity: 
    print("The number is lesser than Negative Infinity!") 
else: 
    print("Negative Infinity is least") 
```

## Script 9 - List Comprehensions
Saving the best for last...these next two are core to the language itself. First, List Comprehensions--say goodbye to multi-line for loops :grin:
```
# Simple List Append 
a = [] 
for x in range(0,10): 
    a.append(x) 
print(a) 
  
# List Comprehension 
print([x for x in a]) 
```

## Script 10 - The Slice Operator
And finally the Slice Operator. Praised as a one of its main benefits over more verbose languages, Python's out of the box Slice Operator quickly sections a list, string, or tuple into a subset defined with some clever syntax. Try this out...you will use it a lot:
```
# Slice Operator 
a = [1,2,3,4,5] 
  
print(a[0:2]) # Choose elements [0-2), upper-bound noninclusive 
  
print(a[0:-1]) # Choose all but the last 
  
print(a[::-1]) # Reverse the list 
  
print(a[::2]) # Skip by 2 
  
print(a[::-2]) # Skip by -2 from the back 
```