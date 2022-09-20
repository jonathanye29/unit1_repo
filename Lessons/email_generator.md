# Email Generator

```.py
import random
random = random.randint(1, 9)

age = int(input("Please type your age: "))
firstname = input("Please type your first name: ")
lastname = input("Please type your last name: ")
grad = int(input("Please type your graduation year (ex: 2020): "))

print(f"Your UWC ISAK Email: {grad}.{firstname}.{lastname}.{random}@uwcisak.jp")
```


![](email_generator.jpg)
