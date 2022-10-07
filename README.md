# Unit-1 Project: Crypto Wallet

![](software-wallet.gif)
<sub>Illustration: Wallet by Katie Horbal</sub>

# Criteria A: Planning

## Problem definition

Ms. Sato is a local trader who is interested in the emerging market of cryptocurrencies. She has started to buy and sell electronic currencies, however at the moment she is tracking all her transactions using a ledger in a spreadsheet which is starting to become burdensome and too disorganized. It is also difficult for Ms. Sato to find past transactions or important statistics about the currency. Ms Sato is in need of a digital ledger that helps her track the amount of the cryptocurrency, the transactions, along with useful statistics. 

Apart for this requirements, Ms Sato is open to explore a cryptocurrency selected by the developer.

An example of the data store is:

| Date | Description | Category | Amount  |
|------|-------------|----------|---------|
| Sep 23 2022 | Purchased groceries | Food | 0.073 MKR |
| Sep 24 2022 | Purchased a new car | Expenses | 116.79 MKR |

## Proposed Solution

Design statement:
I will to design and make a digital ledger for a client who is struggling to keep track of her transaction history. The digital ledge will not only allow my client to keep track of her transactions, she will be able to deposit and withdraw funds from her wallet, and also create new transactions. The Crypto Wallet will provide an easy and efficient way for her to deposit and withdraw funds and create transcations. Further, the digital ledger includes an organized and visually appealing sheet and bar graph displaying the transaction history. This digital ledger is constructed using the software Python and it will take about 35 hours to complete and will be evaluated according to the criteria given.

Maker (MKR) is a smart contract platform built on the Ethereum blockchain that aims to solve volatility issues for the crypto market. It is the basis for a new-generation blockchain-based banking system that allows for faster and simpler international payments and peer-to-peer transactions. Maker aims to unlock the potential of decentralized finance by building an inclusive platform for economic empowerment that gives everyone equal access to the global financial marketplace.

Citations: 
https://www.coinbase.com/price/maker
https://www.abra.com/cryptocurrency/maker/#:~:text=What%20is%20Maker%20coin%3F,peer%2Dto%2Dpeer%20transactions.

Justify the tools/structure of your solution

## Success Criteria
1. The electronic ledger is a text-based software (Runs in the Terminal).
2. The electronic ledger display the basic description of the cyrptocurrency selected.
3. The electronic ledger allows to enter, withdraw and record transactions.
4. The electronic ledger can only be accessed by the client through a set and encrypted password.
5. The electronic ledger will display all past transactions.
6. The electronic ledger will show data about her expenses using a bar graph.

# Criteria B: Design

## System Diagram

![](u1project_sysdiagram.jpg)
Fig 1. System diagram for the program. It shows the input/outputs and software/hardware requirements. The diagram shows how the program runs on Python and shows the different databases the code exchanges information.

## Flow Diagrams

![](u1projectflowdiagram1.jpg)
Fig 2. The flow diagram is for calculating the total balance the user has in their account according to their deposit and withdrawal history. The code will open and read both "balance.csv" and "withdraw.csv" files to see the data inside, and then calculate the difference to find the current balance and converted amount (USD).

![](u1projectflowdiagram2.jpg)
Fig 3. The flow diagram is for calculating up all past transactions and printing them out onto an organized spreadsheet. The code will open up a file called "sheet.csv" which is where all the transaction data is stored and entered into. It will read the file and split the data into the three parts. The date, expense, and transaction amount.


![](u1projectflowdiagram3.jpg)
Fig 4. The flow diagram is for displaying the bar graph with all the transaction totals. It calculates the total amount of money spend in each expense and displays them in an organized categorized bar graph.


## Test Plan
| Test Type | Target | Procedure | Expected Outcome |
|-----------|--------|-----------|------------------|
| Functional: Unit testing | validate_int_input | 1. Use the function validate_int_input 2. Enter a letter in the terminal 3. Enter a number in the terminal | 1. With a letter an error message will be print 2. With a number the program will exit. |
| Functional: Integrational testing | Register system | 1. Use the function register. 2. Enter a desired username and password in the terminal | After entering a desired username and password, the crendtials should go into a database file to store the credentials. It should also print "Registeration Successful!" after the username and password is entered.
| Functional: Integrational testing | Login system | 1. Use the function login. 2. Enter your credentials (username and password) in the terminal | If the username and passwords match with the credentials stored in the database file from the registrations, the code should continue by printing, "Welcome to your Crypto Wallet (username)!". If the username and password entered does not match any of the crendentials stored in the database file, access will be denied to the user and the program will close. 
| Functional : Integrational testing | Create a transaction | 1. Choose to create a transaction 2. Enter the date: Input day, month, year 3. Enter expense category 4. Enter expense amount, price 5. Choose to view transaction history | After choosing the option to create a transaction, the user should be given the ability to choose what the expense was (5 options: Food, Daily, Rent, Travel, Other). Then the user should be given the ability to input a day, month, and year of when the transaction occured. Finally, they can input how much the expense was. All this data should be stored into the database file named "sheet.csv" where all transaction data is organized, so when the user chooses to view their transaction history, they can see a spreadsheet and bar graph of all their transactions. |
| Non-functional: Load testing | Testing if the spreadsheet and bar graph in the transaction history shows all data without any glitches or bugs and does not take a long time to laod. Additionally, all newly inputted transaction data should be displayed well. | 1. Login to the Crypto Wallet 2. Select Create or View Transaction History option 3. Select View transaction history | All information in the spreadsheet should be appropriate to which column it falls under and all information in the bar graph should be appropiate to which row it belongs to. Furthermore, any new transactions the user inputted should be added to the spreadsheet and bar graph. |
| Non-functional: Usuability testing | The login instructions and options displayed in main menu after logging in are clear and easy to read and the directions are easy to follow | 1. Run program 2. Login | The login instructions are clearly displayed, and the main menu items can be easily read, and directions are simple and easy to follow. | 
| Non-functional: Response time | Testing if code responds quickly to user input | 1. Login to the Crypto Wallet 2. Choose any options and follow the prompted directions that follow | The code runs smoothly without crashing or severe lag. The program responds promptly to user input and displays accurate information. | 

## Record of Tasks
| Task No | Planned Action | Planned Outcome | Time estimate | Target completion date | Criterion |
|---------|----------------|-----------------|---------------|------------------------|-----------|
| 1 | Meet withe the client | Talk with the client to dicuss the problems they are facing and brainstorm solutions to create a plan to help the client resolve the problems| 10 minutes | Sep 23 | A |
| 2 | Brainstorm and write the problem definition	| A clear problem definition on Github	| 15 minutes | Sep 23 | A |
| 3 | Brainstorm and write down success criterias | A clear success criteria that suits the client and resolves the problem | 15 minutes | Sep 23 | A |
| 4 | Brainstorm and write down a proposed solution for the client| A clear justification that suits the client and developer.| 15 minutes | Sep 23 | A |
| 5 | Create system diagram | To have a clear idea of the hardware and software requirements for the proposed solution | 45 minutes | Sep 23| B | 
| 6 | Create a simple registration and login system | To create a program that allows the user to register and login to their digital ledger using a username and password they set up | 1 hour minutes| Sep 26| C | 
| 7 | Encrypt the password | A program to protect the application using a password with encryption | 45 minutes | Sep 28 | C |
| 8 | Code the menu of the Crypto Wallet | To have a menu system that includes the title and menu items on the screen | 20 minutes | Sep 30 | C |
| 9 | Code menu options and allow user interaction | The user can choose different options from the menu (Ex: Option 1: Record transcation, and the user will be able to choose Option 1 to record a transaction). | 2 hours | Oct 1 | C | 
| 10 | Create visual display of expense data | Code a bar graph that includes all expense history in categories. | 20 minutes | Oct 1 | C |
| 11 | Create a visual display for transaction data | Code a chart that includes all transaction data with the date, expense, and amount. | 45 minutes | Oct 2 | C |
| 12 | Code a menu for deposit and withdraw | Code a second menu that gives the user two options: Deposit and Withdraw. | 15 minutes | Oct 2 | C |
| 13 | Display correct balance after money is either deposited or withdrawn | Code a function that would add or subtract the amount of money deposited or withdrawn from the balance and print the updated balance | 1 hour | Oct 3 | C |
| 14 | Code a menu for creating or viewing transactions | Code a second menu that gives the user two options: Create a transaction, View transaction history. | 15 minutes | Oct 4 | C |
| 15 | Code transaction functions | Create a code that allows the user to record when they made the transaction, what kind of transaction it was, and how much the transaction was. The code will then transfer all of that information into a spreadsheet and bar graph, with accurate data | 1 hour | Oct 4 | C |
| 16 | Make sure to validate user input for all option choices | Code functions that would make sure what the user inputs follows the requirements (Ex: If a number digit is required but user enters a character, an error message will print, and allowing them to retry). | 1 hour 30 minutes | Oct 5 | C | 
| 17 | Hide the password when it is being typed | The user will only see asteriks when entering their password to increase security. | 45 minutes | Oct 5 | C |
| 18 | Draw and describe the flow diagrams | Flow diagrams for different parts of the solution along with a brief explanation | 1 hour | Oct 6 | B |
| 19 | Write the test plans | Procedures one should take to test the program and the expected outcome of each test is on Github | 1 hour | Oct 7 | B |
| 20 | Meet with client | Hear feedback from the client about the current state of the product | 30 minutes | Oct 7 | B | 
| 21 | Finish Criteria C | Write the descriptions of the code and the detail of the techniques that were used on Github | 2 hours | Oct 7 | C |

# Criteria C: Development

## Techniques Use:
1. Functions
2. For/while loops
3. Input Validation
4. If statements
5. Encryption


## User registration

```.py
import hmac


def register(uname:str, password:str):
    '''
    This function saves a user, password in the file
    credentials.csv
    :param uname: username a string
    :param password: password a string
    :return: nothing
    '''

    #open the file in mode append: a
    file = open("credentials.csv", "a")
    salty = "¯\(°_O)/¯"
    to_hash = uname + password + salty
    hashed_password = hmac.new(''.encode(), to_hash.encode(), 'sha512').hexdigest()
    file.write(f"{uname},{hashed_password}\n")
```

The first part of creating a digital ledger for a client is to create a registration system so the client can create a Crypto Wallet account. This code allows the user to enter a username and password they desire, and it adds their crendentials into a file with and encrypted password. The encryption I used in this is called "hashing". Encryption is the process of encoding plain text or any information in such a way that only authorized people can read it with a corresponding key, like a password, so that confidential data can be protected from unauthorized persons. Hashing converts any amount of data into a fixed-length hash that cannot be reversed. In my code, it is hashed using a random string of characters, known as a salt. This is an additional input to my code above to hash the user's password.


## User login

```.py
def login(username:str, password:str) -> bool:
    """This function receives a username and a password and returns 'ACCESS GRANTED'
    if the username is in the database and the password is correct, otherwise returns 'ACCESS DENIED'"""

    with open("credentials.csv", "r") as file:
        database = file.readlines()
    salty = "¯\(°_O)/¯"
    to_hash = username + password + salty
    hashed_password = hmac.new(''.encode(), to_hash.encode(),  'sha512').hexdigest()
    output = f'{colors[1]}{fonts[0]}ACCESS DENIED{end_code}'.center(50, "-")
    exit_condition = True


    for line in database:
       line_cleaned = line.strip()
       user, password = line_cleaned.split(",")
       if user == username and password == hashed_password:
           output = f"{colors[2]}{fonts[0]}Welcome to your Crypto Wallet {user}!{end_code}".center(66, "-")
           exit_condition = False
           break
    if exit_condition:
        exit(f'{colors[1]}{fonts[0]}ACCESS DENIED{end_code}'.center(50, "-"))
    return output
```

The code above is the program used to allow the client to login to their Crypto Wallet with their registered credentials. The code opens the file where the credntials are stored, and compares whether the entered crendentials match with the registered credentials. If the username and passwords match, it will grant the user access to their Crypto Wallet, and if they don't, they will not gain access to the Crypto Wallet.


## Welcome and main menu

```.py
welcome_msg = "Crypto Wallet".center(50, "=")
prompt_msg = "Please enter an option [1-5]: "

print(f"{colors[7]}{fonts[3]}{welcome_msg}{end_code}")
print("Options".center(50))

menu = """1. View Wallet Balance
2. Deposit or Withdraw Funds
3. Create or view transaction history
4. View Basic Description of the Cryptocurrency
5. Exit
"""
print(menu)

option = validate_int_input(prompt_msg)
    while option > 5 or option < 1:
        option = validate_int_input(f"{colors[1]}Invalid option.{prompt_msg}{end_code}")
```

After the user logs into their crypto wallet, they will be greeted with a welcome message. After that, I created the main menu where the user can access all compotents of their crypto wallet. There are 5 options and I give the user the ability to choose which menu option by letting them input a number between 1-5. In this menu function, if the user does not input a number in the range of 1-5 or they type any other characters, the code will let them try again by letting them know that their input was invalid.


## Current wallet balance

```.py
    if option == 1:
        with open("balance.csv", "r") as file:
            balance = file.readlines()
        with open("withdraw.csv", "r") as file:
            withdraw = file.readlines()
        balance[0] = balance[0].strip()
        taken = 0
        wallet = 0
        for i in balance:
            wallet += int(i)
            converted = int(wallet) * float(144.75)
        for x in withdraw:
            taken += int(x)
            converted = int(wallet) * float(144.75)
        total = wallet - taken
        if total < 0:
            print(f"{colors[1]}{fonts[0]}You have a negative balance of {total}MKR.{end_code}")
        else:
            print(f"{colors[7]}You have a current balance of {colors[2]}{total}MKR{end_code}, which is worth {colors[2]}${converted} USD{end_code {end_code}")
```

This is the code for the first menu option. If the user selects option 1 from the main menu, this is the code that will run. It opens both database files "balance.csv" and "withdraw.csv" as files and reads them. What this does is read all of the data inside of the files. To display the correct wallet balance, I coded the program to subtract the original wallet balance by the amount of money withdrawn. Not only does this code display the regular cryptocurrency balance, it also displays the converted value of the amount of cryptocurrency they have. Further, the program will tell the user if they have a negative balance.


## Deposit or withdraw

```.py
    if option == 2:
        transmenu = """1. Deposit
2. Withdraw"""
        print(transmenu)
        transmenu = validate_int_input('Please enter an option [1-2]: ')
        while transmenu > 2 or transmenu < 1:
            transmenu = validate_int_input(f"{colors[1]}Invalid option. Please enter an option [1-2]: {end_code}")

        if transmenu == 1:
            with open("balance.csv", "a") as file:
                deposit = validate_int_input("How much MKR would you like to deposit?: (ex. 10): ")
                file.write(f'{deposit}\n')
                print(f"{colors[2]}{fonts[0]}You have deposited {deposit}MKR into your wallet.{end_code}")

        if transmenu == 2:
            with open("withdraw.csv", "a") as file:
                withdraw = validate_int_input("How much MKR would you like to withdraw?: (ex. 10): ")
                file.write(f'{withdraw}\n')
                print(f"{colors[2]}{fonts[0]}You have withdrawn {withdraw}MKR from your wallet.{end_code}")
```

Above is the code that allows the user to choose between deposting or withdrawing funds. The data will be stored in the "balance.csv" and "withdraw.csv" files. The code allows the user to deposit or withdraw funds using an "if" statement. The "if" statement checks which option the user inputs. If they input "1", they are choosing option 1, which lets them deposit money. If they input "2", they are choosing option 2, which lets them withdraw money.


## Transaction history spreadsheet

```.py
with open("sheet.csv", "r") as file:
    sheet = file.readlines()
    print('Transaction history:')
    print('-' * 60)
    print('|  Date(MM/DD/YYYY)  |  Expense  | Transaction amount (MKR)|')
    print('-' * 60)




food = 0
daily = 0
rent = 0
travel = 0
other = 0
for l in sheet:
    l = l.strip()
    line1 = l.split(",")
    date = line1[0]
    cat = line1[1]
    price = line1[2]
    print(f'|{date.center(20, " ")}|{cat.center(11, " ")}|{price.center(25, " ")}|')
    print('-' * 60)
```

The code above prints out the users recorded transactions into an organized spreadsheet. It is able to print all recent transactions created by the user by using a for loop. With the for loop, it will continue to go through the data in the "sheet.csv" file and print the data into an organized spreadsheet with all the data in the appropiate column until there is no more data to print. 

## Transaction history bar graph 

```.py
# Adding up the prices
if cat.lower() in "food":
    food += int(price)

elif cat.lower() in "daily":
    daily += int(price)

elif cat.lower() in "rent":
    rent += int(price)

elif cat.lower() in "travel":
    travel += int(price)

else:
    other += int(price)

# Bar graph of expenses
data = [
    ('Food', food),
    ('Daily', daily),
    ('Rent', rent),
    ('Travel', travel),
    ('Other', other),
]

max_value = max(count for _, count in data)
increment = max_value / 25

longest_label_length = max(len(label) for label, _ in data)

for label, count in data:

    bar_chunks, remainder = divmod(int(count * 8 / increment), 8)
    bar = '█' * bar_chunks

    if remainder > 0:
        bar += chr(ord('█') + (8 - remainder))

    bar = bar or '▏'

    print(f'{colors[7]}{label.rjust(longest_label_length)} ▏ {count:#4d} {bar}{end_code}')
```

The code above prints out the users recorded transactions into an organized bar graph. The bar graph code follows the code from the spreadsheet, taking the same data from the file "sheet.csv". It finds the category of expense using "if" and "elif" statements. It groups up all of the numbers into the given categories, and then adds them up accordingly. The bar graph is produced using the number data gathered with a for loop. It prints out each category in a different row, and the displays the bar based off of the total prices added up. The larger the total, the longer the bar will be and vice versa. 


## Printing information about the cryptocurrency

```.py
    if option == 4:
        print(f"{colors[7]}4. Information about your cryptocurrency Maker (MKR):{end_code}")
        info = '''Maker (MKR) is a smart contract platform built on the Ethereum blockchain that aims to solve 
volatility issues for the crypto market. It is the basis for a new-generation blockchain-based banking system 
that allows for faster and simpler international payments and peer-to-peer transactions. Maker aims to unlock 
the potential of decentralized finance by building an inclusive platform for economic empowerment that gives 
everyone equal access to the global financial marketplace. 
'''
        print(f"{colors[9]}{info}{end_code}")
```

This is just a simple print function. Using an "if" statement, if the user inputs "4" from the main menu options, it will run this code and print the information about their cryptocurrency.


## Exiting the program

```.py
if option == 5:
        print(f"{colors[6]}Exiting...{end_code}")
        print(f"{colors[7]}{fonts[3]}See you soon!{end_code}".center(50, "="))
        exit()
```

This is a simple print function that prints a message and exits the program. Using an "if" statement, if the user inputs "5" from the main menu options, it will run this code and print a farewell message and exit the code. 


## Returning to main menu

```.py
state =input("Would you like to return to the main menu? If no, we will exit you from your Crypto Wallet. [yes/no]: ")
    while not state.lower() in ["yes", "no"]:
        state = input(f"{colors[1]}{state} is incorrect. Would you like to return to the main menu? If no, we will exit you from your Crypto Wallet. [yes/no]: {end_code}")

    else:
        if state.lower() == "yes":
            welcome_msg = "Crypto Wallet".center(50, "=")
            print(f"{colors[7]}{fonts[3]}{welcome_msg}{end_code}")
            print("Options".center(50))

            menu = """1. View Wallet Balance
2. Deposit or Withdraw Funds
3. Create or View Transaction History
4. View Basic Description of the Cryptocurrency
5. Exit
"""
            print(menu)
            Main()
        else:
            thankyoumsg = "See you soon!".center(50, "=")
            print(f"{colors[6]}Exiting...{end_code}")
            print(f"{colors[7]}{fonts[3]}{thankyoumsg}{end_code}")
            exit()
```

This code runs after the user finishes completing the desired action. For example, if the user wishes to view their current balance, they will choose option 1, and then this code above will run. It works using a "while" statement, where if what the user inputs matches what the code is asking for. Further, it uses an "if" statement, which allows the code to know whether to exit the program or return the user to the main menu.


# Citations
1. “How to Hash Passwords in Python.” GeeksforGeeks, 22 June 2022, www.geeksforgeeks.org/how-to-hash-passwords-in-python/. Retrieved September 28
2. “Drawing Ascii Bar Charts.” Drawing ASCII Bar Charts –, alexwlchan.net/2018/05/ascii-bar-charts/. Retrieved October 1
