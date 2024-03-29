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


## Minimum of three numbers
Given three integers, print the smallest value.


```.py
a = int(input())
b = int(input())
c = int(input())
if a <= b and b <= c:
    print(a)
elif b <= a and b <= c:
    print(b)
else:
    print(c)
```


![](chp3_snakify_task12.jpg)


## Equal numbers
Given three integers, determine how many of them are equal to each other. The program must print one of these numbers: 3 (if all are the same), 2 (if two of them are equal to each other and the third is different) or 0 (if all numbers are different).


```.py
a = int(input())
b = int(input())
c = int(input())

if a == b and a == c and b == c:
    print("3")
elif a == b or a == c or c == b:
    print("2")
else:
    print("0")
```


![](chp3_snakify_task13.jpg)


## Rook move
Chess rook moves horizontally or vertically. Given two different cells of the chessboard, determine whether a rook can go from the first cell to the second in one move.
The program receives the input of four numbers from 1 to 8, each specifying the column and row number, first two - for the first cell, and then the last two - for the second cell. The program should output YES if a rook can go from the first cell to the second in one move, or NO otherwise.


```.py
column1 = int(input())
row1 = int(input())
column2 = int(input())
row2 = int(input())

if (column1 == column2) or (row1 == row2):
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task14.jpg)


## Chess board - black square
Given a square of a chessboard. Print BLACK if it's black and print WHITE otherwise.
The program receives two numbers from 1 to 8 each - the column and the row number of the square.


```.py
square1 = int(input())
square2 = int(input())

if (square1 % 2 != 0 and square2 % 2 == 0) or (square1 % 2 == 0 and square2 % 2 != 0):
    print('WHITE')
else:
    print('BLACK')
```


![](chp3_snakify_task15.jpg)


## Chess board - same color
Given two cells of a chessboard. If they are painted in one color, print the word YES, and if in a different color - NO.
The program receives the input of four numbers from 1 to 8, each specifying the column and row number, first two - for the first cell, and then the last two - for the second cell.


```.py
tile1x = int(input())
tile1y = int(input())
tile2x = int(input())
tile2y = int(input())

if (tile1x + tile1y) % 2 == 0 and (tile2x + tile2y) % 2 == 0:
    print('YES')
elif (tile1x + tile1y) % 2 != 0 and (tile2x + tile2y) % 2 != 0:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task16.jpg)


## Distance to closest point
Given the coordinates of the three points A, B, and C on a line. Print a distance from the point A to closest point to it.


```.py
a = int(input())
b = int(input())
c = int(input())
distance1 = abs(b - a)
distance2 = abs(c - a)
if distance1 < distance2:
    print(distance1)
if distance2 < distance1:
    print(distance2)
```


![](chp3_snakify_task17.jpg)


## Digits in ascending order
Given a three-digit integer, print YES if its digits go in ascending order, print NO otherwise.


```.py
a = int(input())
digit1 = a // 100
digit2 = a % 100 // 10 
digit3 = a % 100 % 10

if digit1 < digit2 < digit3:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task18.jpg)


## Four-digit palindrome
A palindrome is a number which reads the same when read forward as it it does when read backward. Given a four-digit integer, print "YES" if it's a palindrome and print "NO" otherwise.


```.py
a = int(input())
thousand = a // 1000
hundred = a // 100 % 10
ten = a % 1000 % 100 // 10
one = a % 1000 % 100 % 10
if thousand == one and hundred == ten:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task19.jpg)


## King Move
Chess king moves horizontally, vertically or diagonally to any adjacent cell. Given two different cells of the chessboard, determine whether a king can go from the first cell to the second in one move.
The program receives the input of four numbers from 1 to 8, each specifying the column and row number, first two - for the first cell, and then the last two - for the second cell. The program should output YES if a king can go from the first cell to the second in one move, or NO otherwise.


```.py
tile1x = int(input())
tile1y = int(input())
tile2x = int(input())
tile2y = int(input())
s1 = abs(tile1x - tile2x)
s2 = abs(tile1y - tile2y)

if s1 <= 1 and s2 <=1:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task20.jpg)


## Bishop moves
In chess, the bishop moves diagonally, any number of squares. Given two different squares of the chessboard, determine whether a bishop can go from the first to the second in one move.
The program receives as input four numbers from 1 to 8, specifying the column and row numbers of the starting square and the column and row numbers of the ending square. The program should output YES if a Bishop can go from the first square to the second in one move, or NO otherwise.


```.py
x1 = int(input())
y1 = int(input())
x2 = int(input())
y2 = int(input())
if abs(x1 - x2) == abs(y1 - y2):
   print('YES')
else:
   print('NO')
```


![](chp3_snakify_task21.jpg)


## Queen move
Chess queen moves horizontally, vertically or diagonally to any number of cells. Given two different cells of the chessboard, determine whether a queen can go from the first cell to the second in one move.
The program receives the input of four numbers from 1 to 8, each specifying the column and row number, first two - for the first cell, and then the last two - for the second cell. The program should output YES if a queen can go from the first cell to the second in one move, or NO otherwise.


```.py
x1 = int(input())
y1 = int(input())
x2 = int(input())
y2 = int(input())
if abs(x1 - x2) == abs(y1 - y2) or x1 == x2 or y1 == y2:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task22.jpg)


## Index of outlier
Given three integers: two are equal to each other and the third one is different. Print the index number of this different one - 1, 2 or 3.


```.py
num1 = int(input())
num2 = int(input())
num3 = int(input())

if num1 == num2:
    print('3')
elif num1 == num3:
    print('2')
else:
    print('1')
```


![](chp3_snakify_task23.jpg)


## Knight move
Chess knight moves like the letter L. It can move two cells horizontally and one cell vertically, or two cells vertically and one cells horizontally. Given two different cells of the chessboard, determine whether a knight can go from the first cell to the second in one move.
The program receives the input of four numbers from 1 to 8, each specifying the column and row number, first two - for the first cell, and then the last two - for the second cell. The program should output YES if a knight can go from the first cell to the second in one move, or NO otherwise.


```.py
x1 = int(input())
y1 = int(input())
x2 = int(input())
y2 = int(input())
if abs(x1 - x2) == 1 and abs(y1 - y2) == 2 or abs(x1 - x2) == 2 and abs(y1 - y2) == 1:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task24.jpg)


## Chocolate bar
Chocolate bar has the form of a rectangle divided into n×m portions. Chocolate bar can be split into two rectangular parts by breaking it along a selected straight line on its pattern. Determine whether it is possible to split it so that one of the parts will have exactly k squares.
The program reads three integers: n, m, and k. It should print YES or NO.


```.py
n = int(input())
m = int(input())
k = int(input())

if ((k % n == 0) or (k % m == 0)) and k < n * m:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task25.jpg)


## Leap year
Given the year number. You need to check if this year is a leap year. If it is, print LEAP, otherwise print COMMON.
The rules in Gregorian calendar are as follows:

a year is a leap year if its number is exactly divisible by 4 and is not exactly divisible by 100
a year is always a leap year if its number is exactly divisible by 400
Warning. The words LEAP and COMMON should be printed all caps.


```.py
year = int(input())
if ((year % 4 == 0) and (year % 100 != 0)) or (year % 400 == 0):
    print('LEAP')
else:
    print('COMMON')
```


![](chp3_snakify_task26.jpg)


## Days in month
Given a month - an integer from 1 (January) to 12 (December), print the number of days in it in the year 2017 (or any other non-leap year).


```.py
month = int(input())
if month == 1 or month == 3 or month == 5 or month == 7 or month == 8 or month == 10 or month == 12:
    print('31')
elif month == 2:
    print('28')
else:
    print('30')
```


![](chp3_snakify_task27.jpg)


## Next day
Given the month (an integer from 1 to 12) and the day in it (an integer from 1 to 31) in the year 2017 (or in any other common year), print the month and the day of the next day to it. The first test corresponds to March 30 and March 31. The second test corresponds to March 31 and April 1.


```.py
a = int(input())
b = int(input())
if a == 1 or a == 3 or a == 5 or a == 7 or a == 8 or a == 10 or a == 12:
    day = 31
elif a == 2:
    day = 28
else:
    day = 30
if day == 31:
    if a == 12 and b == 31:
        print("1")
        print("1")
    elif b == 31:
        print(a + 1)
        print(1)
    else:
        print(a)
        print(b + 1)
if day == 30:
    if b == 30:
        print(a + 1)
        print(1)
    else:
        print(a)
        print(b + 1)
if day == 28:
    if b == 28:
        print(a + 1)
        print(1)
    else:
        print(a)
        print(b + 1)
```


![](chp3_snakify_task28.jpg)


## Linear equation
Write a program that solves a linear equation ax = b in integers. Given two integers a and b (a may be zero), print a single integer root if it exists and print "no solution" or "many solutions" otherwise.


```.py
a = int(input())
b = int(input())
if a == 0 and b == 0:
    print('many solutions')
elif a == 0 and b != 0 or b % a != 0:
    print('no solution')
else:
    print(b // a)
```


![](chp3_snakify_task29.jpg)


## Vertices of Rectangle
Given integer coordinates of three vertices of a rectangle whose sides are parallel to the coordinate axes, find the coordinates of the fourth vertex of the rectangle. In the first test the three given vertices are (1, 4), (1, 6), (7, 4). The fourth vertex is thus (7, 6).


```.py
x1 = int(input())
y1 = int(input())
x2 = int(input())
y2 = int(input())
x3 = int(input())
y3 = int(input())
if x1 == x2:
    x4 = x3
elif x1 == x3:
    x4 = x2
else:
  x4 = x1
if y1 == y2:
    y4 = y3
elif y1 == y3:
    y4 = y2
else:
    y4 = y1
print(x4)
print(y4)
```


![](chp3_snakify_task30.jpg)


## Sort three numbers
Given three integers, print them in ascending order.


```.py
a = int(input())
b = int(input())
c = int(input())

if a > b:
    a, b = b, a
if a > c:
    a, c = c, a
if b > c:
    b, c = c, b

print(a)
print(b)
print(c)
```


![](chp3_snakify_task31.jpg)


## White pawn move
A white chess pawn moves up vertically one square at a time. An exception is a pawn on a row #2: it can move either one or two squares up. In addition, a white chess pawn captures diagonally up one square to the left or right. A white chess pawn can never occur on a row #1.
The program receives the input of four numbers from 1 to 8, each specifying the column and row number, first two - for the first square, and then the last two - for the second square. The program should print YES if a white pawn can possibly move from the first square to the second square in one move in some game - either by move or by capture. The program should print NO otherwise. The first four tests correspond to the green arrows on the picture below.


```.py
x1 = int(input())
y1 = int(input())
x2 = int(input())
y2 = int(input())

if y1 == 1 and y2 == y1 + 1:
    print('NO')
elif x1 == x2 and y2 == y1 + 1 :
    print('YES')
elif y1 == 2 and y2 == 4 and x2 == x1:
    print('YES')
elif (x2 == x1 + 1 or x2 == x1 - 1) and y2 == y1 + 1:
    print('YES')
else:
    print('NO')
```


![](chp3_snakify_task32.jpg)


# Chapter 4
For loop with range


## Count to N
Given an integer N, print all the numbers from 1 to N.


```.py
N = int(input())
for i in range (1, N + 1):
    print(i)
```


![](chp4_snakify_task1.jpg)


## Series - 1
Given two integers A and B (A ≤ B). Print all numbers from A to B inclusively.


```.py
a = int(input())
b = int(input())

for i in range (a , b + 1):
    print(i)
```


![](chp4_snakify_task2.jpg)


## First N odd, ascending
Given an integer N, print all the odd numbers from 1 to N in ascending order.


```.py
n = int(input())

for i in range(1, n + 1, 2):
    print(i)
```


![](chp4_snakify_task3.jpg)


## Series - 2
Given two integers A and B. Print all numbers from A to B inclusively, in ascending order, if A < B, or in descending order, if A ≥ B.


```.py
a = int(input())
b = int(input())

if a < b:
    for i in range(a ,b + 1):
        print(i)
    
elif b < a:
    for i in range(a, b - 1, -1):
        print(i)
        
else:
    print(a)
```


![](chp4_snakify_task4.jpg)


## First N even, descending
Given an integer N, print all the even numbers from 0 to N in descending order.


```.py
n = int(input())

if n % 2== 0:
    for i in range(n, -1, -2):
        print(i)
else:
    for i in range(n - 1, -1, -2):
        print(i)
```


![](chp4_snakify_task5.jpg)


## Sum of ten numbers
10 numbers are given in the input. Read them and print their sum. Use as few variables as you can.


```.py
x = 0
for i in range(10):
    x += int(input())
print(x)
```


![](chp4_snakify_task6.jpg)


## Sum of N numbers
N numbers are given in the input. Read them and print their sum.
The first line of input contains the integer N, which is the number of integers to follow. Each of the next N lines contains one integer. Print the sum of these N integers.


```.py
n = int(input())
ans = 0
for i in range(n):
    ans += int(input())
print(ans)
```


![](chp4_snakify_task7.jpg)


## Product of N numbers
N numbers are given in the input. Read them and print their product.
The first line of input contains a positive integer N: the number of integers to follow. Each of the next N lines contains one integer. Print the product of these N integers.


```.py
n = int(input())
product = 1
for i in range(n):
    product *= int(input())
print(product)
```

![](chp4_snakify_task8.jpg)


## Sum of cubes
For the given integer N calculate the following sum: 1^3+2^3+…+N^3


```.py
n = int(input())
sum = 0
for i in range(1, n + 1):
    sum += i ** 3
print(sum)
```


![](chp4_snakify_task9.jpg)


## Factorial
For the given integer n calculate the value n!. Don't use math module in this exercise.


```.py
n = int(input())
product = 1
for i in range(1, n + 1):
    product *= i
print(product)
```


![](chp4_snakify_task10.jpg)


## The number of zeros
Given N numbers: the first number in the input is N, after that N integers are given. Count the number of zeros among the given integers and print it.
You need to count the number of numbers that are equal to zero, not the number of zero digits.


```.py
n = int(input())
count = 0
for i in range(n):
    if int(input())  == 0:
        count += 1
print(count)
```


![](chp4_snakify_task11.jpg)


## Adding factorials
Given an integer n, print the sum 1!+2!+3!+...+n!.


```.py
n = int(input())
product = 1
sum = 0
for i in range(1, n + 1):
    product *= i
    sum += product
print(sum)
```


![](chp4_snakify_task12.jpg)


## Squares in range
Given two integers A and B, print squares of all integer numbers between them, as shown below. There shouldn't be any spaces around * and =. The sep argument of the function print() may help you with that.


```.py
a = int(input())
b = int(input())
for i in range(a, b + 1):
    print(i, '*', i, '=', i**2, sep = '')
```


![](chp4_snakify_task13.jpg)


## Ladder
For given integer n ≤ 9 print a ladder of n steps. The k-th step consists of the integers from 1 to k without spaces between them.


```.py
n = int(input())
for i in range(1, n + 1):
    for o in range(1, i + 1):
        print(o, end= "")
    print()
```
 

![](chp4_snakify_task14.jpg)


## Is prime
A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. Given an integer N > 1, print PRIME if it's prime and print COMPOSITE otherwise.


```.py
n = int(input())
result = 'PRIME'
for i in range(2, n - 1):
    if n % i == 0:
        result = 'COMPOSITE'
print(result)
```


![](chp4_snakify_task15.jpg)


## Print primes in range
A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. Given two integers A and B, print all prime numbers between them, inclusively.


```.py
a = int(input())
b = int(input())
for i in range(a, b + 1):
    if i > 1:
        for j in range(2, i):
            if (i % j) == 0:
                break
        else:
            print(i)
```


![](chp4_snakify_task16.jpg)


## Number of primes in range
A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. Given two integers A and B, print the number of primes between them, inclusively.


```.py
a = int(input())
b = int(input())
def prime(n):
    if n <= 1:
        return False
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
count = 0
for i in range(a, b + 1):
    if prime(i):
        count += 1
print(count)
```


![](chp4_snakify_task17.jpg)


## Lost card
There was a set of cards with numbers from 1 to N. One of the card is now lost. Determine the number on that lost card given the numbers for the remaining cards.
Given a number N, followed by N − 1 integers - representing the numbers on the remaining cards (distinct integers in the range from 1 to N). Find and print the number on the lost card.


```.py
n = int(input())
sum = 0
for i in range(n - 1):
    sum += int(input())
print(int(n * (n + 1) / 2 - sum))
```


![](chp4_snakify_task18.jpg)


# Chapter 5
Strings


## Slices
You are given a string.
In the first line, print the third character of this string.

In the second line, print the second to last character of this string.

In the third line, print the first five characters of this string.

In the fourth line, print all but the last two characters of this string.

In the fifth line, print all the characters of this string with even indices (remember indexing starts at 0, so the characters are displayed starting with the first).

In the sixth line, print all the characters of this string with odd indices (i.e. starting with the second character in the string).

In the seventh line, print all the characters of the string in reverse order.

In the eighth line, print every second character of the string in reverse order, starting from the last one.

In the ninth line, print the length of the given string.


```.py
string = str(input())
print(string[2])
print(string[-2])
print(string[:5])
print(string[:-2])
print(string[::2])
print(string[1::2])
print(string[::-1])
print(string[::-2])
print(len(string))
```


![](chp5_snakify_task1.jpg)


## The number of words
Given a string consisting of words separated by spaces. Determine how many words it has. To solve the problem, use the method count.


```.py
words = input()
print(words.count(' ') + 1)
```


![](chp5_snakify_task2.jpg)


## The two halves
Given a string. Cut it into two "equal" parts (If the length of the string is odd, place the center character in the first string, so that the first string contains one more characther than the second). Now print a new string on a single row with the first and second halfs interchanged (second half first and the first half second)
Don't use the statement if in this task.


```.py
s = input()
print(s[(len(s) + 1) // 2:] + s[:(len(s) + 1) // 2])
```


![](chp5_snakify_task3.jpg)


## To swap the two words
Given a string consisting of exactly two words separated by a space. Print a new string with the first and second word positions swapped (the second word is printed first).
This task should not use loops and if.


```.py
s = input()
print(s[s.find(' ') + 1:] + ' ' + s[:s.find(' ')])
```


![](chp5_snakify_task4.jpg)


## The first and last occurrence
Given a string that may or may not contain a letter of interest. Print the index location of the first and last appearance of f. If the letter f occurs only once, then output its index. If the letter f does not occur, then do not print anything.
Don't use loops in this task.


```.py
s = input()
if s.count('f') == 1:
    print(str(s.find('f')))
elif s.count('f') > 1:
    print(str(s.find('f')) + ' ' + str(s.rfind('f')))
```


![](chp5_snakify_task5.jpg)


## The second occurrence
Given a string that may or may not contain the letter of interest. Print the index location of the second occurrence of the letter f. If the string contains the letter f only once, then print -1, and if the string does not contain the letter f, then print -2.


```.py
s = input()
if s.count('f') == 1:
    print(-1)
elif s.count('f') == 0:
    print(-2)
else:
    print(s.find('f', s.find('f') + 1))
```


![](chp5_snakify_task6.jpg)


## Remove the fragment
Given a string in which the letter h occurs at least twice. Remove from that string the first and the last occurrence of the letter h, as well as all the characters between them.


```.py
s = input()
if s.count('h') >= 2:
    h = s.find('h')
    print(s[:s.find('h')] + s[s.rfind('h') + 1:])
```


![](chp5_snakify_task7.jpg)


## Reverse the fragment
Given a string in which the letter h occurs at least two times, reverse the sequence of characters enclosed between the first and last appearances.


```.py
s = input()
i = s.find('h')
j = s.rfind('h')
print(s[:i] + s[i:j + 1][::-1] + s[j + 1:])
```


![](chp5_snakify_task8.jpg)


## Replace the substring
Given a string. Replace in this string all the numbers 1 by the word one.


```.py
s = input()
print(s.replace('1', 'one'))
```


![](chp5_snakify_task9.jpg)


## Delete a character
Given a string. Remove from this string all the characters @.


```.py
s = input()
print(s.replace('@', ''))
```


![](chp5_snakify_task10.jpg)


## Replace within the fragment
Given a string. Replace every occurrence of the letter h by the letter H, except for the first and the last ones.


```.py
s = input()
a = s[:s.find('h') + 1] 
b = s[s.find('h') + 1:s.rfind('h')]
c = s[s.rfind('h'):]
s = a + b.replace('h', 'H') + c
print(s)
```


![](chp5_snakify_task11.jpg)


## Delete every third character
Given a string. Delete from it all the characters whose indices are divisible by 3.


```.py
s = input()
t = ''
for i in range(len(s)):
    if i % 3 != 0:
        t = t + s[i]
print(t)
```

![](chp5_snakify_task12.jpg)


# Chapter 6
While loop


## List of squares
For a given integer N, print all the squares of integer numbers where the square is less than or equal to N, in ascending order.


```.py
n = int(input())
i = 1
while i ** 2 <= n:
    print(i ** 2)
    i += 1
```


## Least divisor
Given an integer not less than 2. Print its smallest integer divisor greater than 1.


```.py
n = int(input())
i = 2
while i <= n:
    if n % i == 0:
        print(i)
        break
    i += 1
```


## The power of two
For a given integer N, find the greatest integer x where 2x is less than or equal to N. Print the exponent value and the result of the expression 2x.
Don't use the operation **.


```.py
n = int(input())
x = 1
i = 2
while i <= n:
    i *= 2
    x += 1
print(x - 1, i //2)
```


## Morning jog
As a future athlete you just started your practice for an upcoming event. Given that on the first day you run x miles, and by the event you must be able to run y miles.
Calculate the number of days required for you to finally reach the required distance for the event, if you increases your distance each day by 10% from the previous day.

Print one integer representing the number of days to reach the required distance.


```.py
x = int(input())
y = int(input())
days = 1 
while x < y:
    x = x * 1.1
    days += 1
print(days)
```


## The length of the sequence
Given a sequence of non-negative integers, where each number is written in a separate line. Determine the length of the sequence, where the sequence ends when the integer is equal to 0. Print the length of the sequence (not counting the integer 0). The numbers following the number 0 should be omitted.


```.py
x = int(input())
count = 0
while x != 0:
    x = int(input())
    count += 1
print(count)
```


## The sum of the sequence
Determine the sum of all elements in the sequence, ending with the number 0.


```.py
x = int(input())
sum = 0
while x != 0:
    sum += x
    x = int(input())
print(sum)
```


## The average of the sequence
Determine the average of all elements of the sequence ending with the number 0.


```.py
x = int(input())
sum = 0
count = 0
while x != 0:
    sum += x
    count += 1
    x = int(input())
print(sum / count)
```


## The maximum of the sequence
A sequence consists of integer numbers and ends with the number 0. Determine the largest element of the sequence.


```.py
x = int(input())
max = x
while x != 0:
    x = int(input())
    if x > max:
        max = x
print(max)
```


## The index of the maximum of a sequence
A sequence consists of integer numbers and ends with the number 0. Determine the index of the largest element of the sequence. If the highest element is not unique, print the index of the first of them.


```.py
x = int(input())
i = 0
max = 0
while x != 0:
    i += 1
    if x > max:
        max = x
        index = i
    x = int(input())
print(index)
```


## The number of even elements of the sequence
Determine the number of even elements in the sequence ending with the number 0.


```.py
x = int(input())
count = 0
while x != 0:
    if x % 2 == 0:
        count += 1
    x = int(input())
print(count)
```


## The number of elements that are greater than the previous one
A sequence consists of integer numbers and ends with the number 0. Determine how many elements of this sequence are greater than their neighbours above.


```.py
x = int(input())
count = 0
while x != 0:
    x1 = int(input())
    if x1 > x:
        count += 1
    x = x1
print(count)
```


## The second maximum
The sequence consists of distinct positive integer numbers and ends with the number 0. Determine the value of the second largest element in this sequence. It is guaranteed that the sequence has at least two elements.


```.py
s = []
temp = 1
while temp != 0:
    temp = int(input())
    s.append(temp)
s.sort()
print(s[-2])
```


## The number of elements equal to the maximum
A sequence consists of integer numbers and ends with the number 0. Determine how many elements of this sequence are equal to its largest element.


```.py
x = []
temp = 1
while temp != 0:
    temp = int(input())
    x.append(temp)
print(x.count(max(x)))
```


## Fibonacci numbers
The Fibonacci sequence is defined as follows:
ϕ0=0, ϕ1=1, ϕn=ϕn−1+ϕn−2.
Given a non-negative integer n, print the nth Fibonacci number ϕn.
This problem can also be solved with a for loop.


```.py
n = int(input())
def fib(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fib(n - 1) + fib(n - 2)
print(fib(n))
```


## The index of a Fibonacci number
The Fibonacci sequence is defined as follows:
ϕ0=0, ϕ1=1, ϕn=ϕn−1+ϕn−2.
Given an integer a, determine its index among the Fibonacci numbers, that is, print the number n such that ϕn=a. If a is not a Fibonacci number, print -1.


```.py
 n = int(input())
a = 0
b = 1
c = 0
count = 1
while c < n:
    c = a + b
    a = b
    b = c
    count += 1
if c == n:
    print(count)
else:
    print(-1)
```
 
 
