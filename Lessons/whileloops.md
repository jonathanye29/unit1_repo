# While loops lesson


```.py
number = int(input("Please enter an integer"))
while number > 5:
    number = int(input("Error. Please enter an integer smaller than 5"))
print("Good job")
```


```.py
number = input("Please enter an integer")
max_num_tries = 5
while not number.isdigit() and max_num_tries > 0:
    print(f"Number of chances remaining {max_num_tries}")
    max_num_tries = max_num_tries - 1
    number = input("Error. Please enter an integer")

if max_num_tries != 0:
    print("Hooray. Well done entering an integer")
else:
    exit()
```


![](whileloops.jpg)
