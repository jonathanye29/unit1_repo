
# Chapter 1
Input, print and numbers


## Sum of 3 numbers
Write a program that takes three numbers and prints their sum. Every number is given on a separate line.


```.py
a = int(input())
b = int(input())
c = int(input())
print(a+b+c)
```

![](chp1_snakify_task1.jpg)


## Hi John
Write a program that greets the person by printing the word "Hi" and the name of the person. See the examples below.


```.py
print("Hi " + input())
```


![](chp1_snakify_task2.jpg)


## Square
Write a program that takes a number and print its square.


```.py
a = int(input())
print(a * a)
```


![](chp1_snakify_task3.jpg)


## Area of right-angled triangle
Write a program that reads the length of the base and the height of a right-angled triangle and prints the area. Every number is given on a separate line.


```.py
b = int(input())
h = int(input())
print(b * h / 2)
```


![](chp1_snakify_task4.jpg)


## Hello, Harry!
Write a program that greets the user by printing the word "Hello", a comma, the name of the user and an exclamation mark after it. See the examples below.


```.py
name = input()
print("Hello, " + name + "!")
```

![](chp1_snakify_task5.jpg)


## Two timestamps
A timestamp is three numbers: a number of hours, minutes and seconds. Given two timestamps, calculate how many seconds is between them. The moment of the first timestamp occurred before the moment of the second timestamp.


```.py
h1 = int(input())
m1 = int(input())
s1 = int(input())

h2 = int(input())
m2 = int(input())
s2 = int(input())

h1 = h1 * 3600
m1 = m1 * 60

h2 = h2 * 3600
m2 = m2 *60

time1 = h1 + m1 + s1
time2 = h2 + m2 + s2

print(time2 - time1)
```

![](chp1_snakify_task6.jpg)


## School desks
A school decided to replace the desks in three classrooms. Each desk sits two students. Given the number of students in each class, print the smallest possible number of desks that can be purchased.
The program should read three integers: the number of students in each of the three classes, a, b and c respectively.

In the first test there are three groups. The first group has 20 students and thus needs 10 desks. The second group has 21 students, so they can get by with no fewer than 11 desks. 11 desks is also enough for the third group of 22 students. So we need 32 desks in total.


```.py
class1 = int(input())
class2 = int(input())
class3 = int(input())

desk1 = class1 // 2 + class1 % 2
desk2 = class2 // 2 + class2 % 2
desk3 = class3 // 2 + class3 % 2

print(desk1 + desk2 + desk3)
```

![](chp1_snakify_task7.jpg)


# Chapter 2
Integer and float numbers


## Last digit of integer
Given an integer number, print its last digit.


```.py
a = int(input())
print(a % 10)
```


![](chp2_snakify_task1.jpg)


## Two digits
Given a two-digit number, print its digits separately.


```.py
a = int(input())
print(a // 10 , a % 10)
```


![](chp2_snakify_task2.jpg)


## Swap digits
Given a two-digit number, swap its digits as shown in the tests below.


```.py
a = int(input())
print(str(a % 10) + str(a // 10))
```


![](chp2_snakify_task3.jpg)


## Last two digits
Given an integer number, print its last two digits.


```.py
print(int(input()) % 100)
```


![](chp2_snakify_task4.jpg)


## Tens digit
Given an integer. Print its tens digit.


```.py
a = int(input())
print(a // 10 % 10)
```


![](chp2_snakify_task5.jpg)


## Sum of digits
Given a three-digit number. Find the sum of its digits.


```.py
number = int(input())
a = number // 100
b = number // 10 % 10
c = number % 10
print(a + b + c)
```


![](chp2_snakify_task6.jpg)


## Reverse three digits
Given a three-digit integer number, print its digits in a reversed order.


```.py
a = int(input())
print(str(a % 10) + str(a // 10 % 10) + str(a // 100))
```


![](chp2_snakify_task7.jpg)


## Merge two numbers
Given two two-digit numbers, merge their digits as shown in the tests below.


```.py
a = int(input())
b = int(input())
print(str(a // 10) + str(b // 10) + str(a % 10) + str(b % 10))
```


![](chp2_snakify_task8.jpg)


## Cyclic rotation
Given a four-digit integer number, perform its cyclic rotation by two digits, as shown in the tests below.


```.py
a = int(input())
print(str(a % 100) + str(a // 100))
```


![](chp2_snakify_task9.jpg)


## Fractional part
Given a positive real number, print its fractional part.


```.py
a = float(input())
a = a-int(a)
print(a)
```


![](chp2_snakify_task10.jpg)


## First digit after decimal point
Given a positive real number, print its first digit to the right of the decimal point.


```.py
a = float(input())
b = int((a * 10) % 10)
print(b)
```


![](chp2_snakify_task11.jpg)


## Car route
A car can cover distance of N kilometers per day. How many days will it take to cover a route of length M kilometers? The program gets two numbers: N and M.


```.py
from math import ceil
n = int(input())
m = int(input())
distance = m / n
print(ceil(distance))
```


![](chp2_snakify_task12.jpg)


## Day of week
Let's count the days of the week as follows: 0 - Sunday, 1 - Monday, 2 - Tuesday, ..., 6 - Saturday. Given an integer K in the range 1 to 365, find the number of the day of the week for the K-th day of the year provided that this year's January 1 is Thursday.


```.py
a = int(input())
print((a + 3) % 7)
```

![](chp2_snakify_task13.jpg)


## Digital clock
Given the integer N - the number of minutes that is passed since midnight - how many hours and minutes are displayed on the 24h digital clock?
The program should print two numbers: the number of hours (between 0 and 23) and the number of minutes (between 0 and 59).


```.py
a = int(input())
hour = a // 60
minute = a % 60
print(hour, minute)
```

![](chp2_snakify_task13.jpg)


## Total cost
A cupcake costs A dollars and B cents. Determine, how many dollars and cents should one pay for N cupcakes. A program gets three numbers: A, B, N. It should print two numbers: total cost in dollars and cents.


```.py
a = int(input())
b = int(input())
n = int(input())
cost = n * (100 * a + b)
print(cost // 100, cost % 100)
```


![](chp2_snakify_task15.jpg)


## Century
Given a year as a positive integer, print its century. Mind that the 20th century began on 1901 and ended on 2000.


```.py
a = int(input())
century = (a - 1) // 100 + 1
print(century)
```


![](chp2_snakify_task16.jpg)


## Snail
A snail goes up A feet during the day and falls B feet at night. How long does it take him to go up H feet?
Given three integer numbers H, A and B (A > B), the program should output a number of days.


```.py
from math import ceil

h = int(input())
a = int(input())
b = int(input())
diff = a - b
print(ceil((h - a) / (diff)) + 1)
```


![](chp2_snakify_task17.jpg)


## Clock face - 1
H hours, M minutes and S seconds are passed since the midnight (0 ≤ H < 12, 0 ≤ M < 60, 0 ≤ S < 60). Determine the angle (in degrees) of the hour hand on the clock face right now.


```.py
H = int(input())
M = int(input())
S = int(input())
A = 360 / 12 * H
A = A + (360 / 12 / 60 * M)
A = A + (360 / 12 / 3600 * S)
print(A)
```


![](chp2_snakify_task18.jpg)


## Clock face - 2
Hour hand turned by α degrees since the midnight. Determine the angle by which minute hand turned since the start of the current hour. Input and output in this problems are floating-point numbers.


```.py
a = float(input())
a = (a % (360 / 12))
print(a / 60 * 360 * 2)
```


![](chp2_snakify_task19.jpg)


# Chapter 3
Conditions: if, then, else


## Is positive
Given an integer, print "YES" if it's positive and print "NO" otherwise.


```.py
x = int(input())
if x > 0:
    print("YES")
else:
    print("NO")
```


![](chp3_snakify_task1.jpg)


## Is odd
Given an integer, print "YES" if it's odd and print "NO" otherwise.


```.py
a = int(input())
if a % 2 == 0:
    print("NO")
else:
    print("YES")
```


![](chp3_snakify_task2.jpg)


## Is even
Given an integer, print "YES" if it's even and print "NO" otherwise.


```.py
a = int(input())
if a % 2 == 0:
    print("YES")
else:
    print("NO")
```


![](chp3_snakify_task3.jpg)


## Ends on seven
Given an integer, print "YES" if it's last digit is 7 and print "NO" otherwise.


```.py
a = int(input())
if a % 10 == 7:
    print("YES")
else:
    print("NO")
```


![](chp3_snakify_task4.jpg)


## Minimum of two numbers
Given two integers, print the smaller value.


```.py
a = int(input())
b = int(input())
if a < b:
    print(a)
else:
    print(b)
```

![](chp3_snakify_task5.jpg)


## Are both odd
Given two integers, print "YES" if they're both odd and print "NO" otherwise.


```.py
a = int(input())
b = int(input())
if a % 2 != 0 and b % 2 != 0:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task6.jpg)


## At least one odd
Given two integers, print "YES" if at least one of them is odd and print "NO" otherwise.


```.py
a = int(input())
b = int(input())
if a % 2 != 0 or b % 2 != 0:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task7.jpg)


## Exactly one odd
Given two integers, print "YES" if exactly one of them is odd and print "NO" otherwise.


```.py
a = int(input())
b = int(input())
if (a % 2 != 0 and b % 2 == 0) or (a % 2 == 0 and b % 2 != 0):
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task8.jpg)


## Sign function
For the given integer X print 1 if it's positive, -1 if it's negative, or 0 if it's equal to zero.
Try to use the cascade if-elif-else for it.


```.py
a = int(input())
if a > 0:
    print('1')
elif a < 0:
    print('-1')
else:
    print('0')
```


![](chp3_snakify_task9.jpg)


## Numbers in ascending order
Given three different integers, print YES if they're given in ascending order, print NO otherwise.


```.py
a = int(input())
b = int(input())
c = int(input())
if a < b < c:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task10.jpg)


## Is three digit
Given an integer, print "YES" if it's a three-digit number and print "NO" otherwise.


```.py
number = int(input())
if 100 <= number <= 999:
    print("YES")
else:
    print("NO")
```


![](chp3_snakify_task11.jpg)


