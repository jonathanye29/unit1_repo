# For loop basics

```.py
# 1-repeating a number of times steps of 1
for i in range (0, 10, 1):
    print(i)
# 2
for i in range(10, -1, -1):
    print(i)

#3 count from 2000 to 2020 in steps of 3
for year in range(2000, 2020, 3):
    print(f"This produces the sames years {year}")

#4 looping over a list of elements
for names in ["bob", "alice", "carla", "dvaid"]:
    print(names)

#5 loop over letters
for let in "This is a message":
    print(let)

#6 loops inside a loop or Nested loops
num = 1
for row in range(3):
    for col in [0,1,2,3]:
        print(str(num).center(4), end=" ")
        num += 1
    print("")
```
