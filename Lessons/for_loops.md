# For Loops

```.py
x = [[3, 8], ['bob', '30'], 5, 'alice']
index = 0
while index < len(x):
    print(x[index])
    index += 1
#---------------------
x = [[3, 8], ['bob', '30'], 5, 'alice']
for item in x:
    print(item)
#------------
x = [[3, 8], ['bob', '30'], 5, 'alice']
index = 0
for item in x:
    print(f'Item #{index}: {item}')
    index += 1
#----------------------------
numbers = []
numbers = list()

value = 0
while value < 100:
    numbers.append(value)
    print(numbers)
    value += 1
```


![](sep8lesson.jpg)
