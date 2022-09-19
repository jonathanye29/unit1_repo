# Programming Task 1

## Task 1
Create a program and the flow diagram that shows the colors of all the lockers from 1 to 2400


```.py
number_lockers = 2400

for locker in range(1, number_lockers + 1, 1):
    color_code = locker % 4
    if color_code == 0:
        color = "Red"
    if color_code == 1:
        color = "White"
    if color_code == 2:
        color = "Yellow"
    if color_code == 3:
        color = "Blue"
    number_chars = 50
    char = '.'
    color_centered = color.center(number_chars, char)
    print(f"Locker No {locker} is color {color_centered}")
```


![](prgmtask1_task1.jpg)


Flow chart:

![](prgmtask1_task1flowchart.jpg)


## Task 2


```.py
locker_number = int(input("Please enter locker number: "))

if locker_number <= 2400:
    color_code = locker_number % 4
    if color_code == 0:
        color = "Red"
    if color_code == 1:
        color = "White"
    if color_code == 2:
        color = "Yellow"
    if color_code == 3:
        color = "Blue"
    number_chars = 50
    char = '.'
    color_centered = color.center(number_chars, char)
    print(f"Locker No {locker_number} is color {color_centered}")
 ```
 
 
 ![](prgmtask1_task2.jpg)
 
 
 ## Task 3
 
 
 ```.py
 color_input = input("What color (red, white, yellow, or blue) is the locker? ")

for locker in range(1, 2401):
    number = locker % 4
    if color_input == "red":
        if number == 0:
            print(locker)
    if color_input == "white":
        if number == 1:
            print(locker)
    if color_input == "yellow":
        if number == 2:
            print(locker)
    if color_input == "blue":
        if number == 3:
            print(locker)
 ```
 
 
 ![](prgmtask1_task3.jpg)
 
 
 ## Task 4


