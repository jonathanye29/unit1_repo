# Number counter


```.py
max_num_tries = 5
start = input("please type an integer you would like to start at: ")
while not start.isdigit() and max_num_tries > 0:
    max_num_tries = max_num_tries - 1
    print(f"Number of chances remaining {max_num_tries}")
    start = input("Error. Please enter an integer for the start: ")
if max_num_tries > 0:
    start = int(start)
else:
    exit()

limit = input("Please type an integer you would like the code to count to: ")
while not limit.isdigit() and max_num_tries > 0:
    max_num_tries = max_num_tries - 1
    print(f"Number of chances remaining {max_num_tries}")
    end = input("Error. Please enter an integer for the limit: ")
if max_num_tries > 0:
    limit = int(limit)
else:
    exit()

step = input("Please type an interval you would like to count in (integer): ")
while not step.isdigit() and max_num_tries > 0:
    max_num_tries = max_num_tries - 1
    print(f"Number of chances remaining {max_num_tries}")
    step = input("Error. Please enter an integer for the step: ")
if max_num_tries > 0:
    step = int(step)
else:
    exit()

print(f"Now counting from {start} to {limit} by {step}s")
while start <= limit:
    print(start)
    start = start + step

while start >= limit:
    print(start)
    start = start - step
```


![](numbercounter.jpg)
