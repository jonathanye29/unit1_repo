# Project 1: Crypto Wallet


```.py
# Success Criteria:
# The electronic ledger is a text-based software (Runs in the Terminal).
# The electronic ledger display the basic description of the cyrptocurrency selected.
# The electronic ledger allows to enter, withdraw and record transactions.
# The electronic ledger can only be accessed by the client through a set password.
# The electronic ledger will display all past transactions.
# The electronic ledger will show data about her expenses using a bar graph: Each color represents a certain expense.
# This is the clean and organized code for Unit 1 Project

from project_lib import validate_int_input, colors, fonts
import hmac

colors = ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;34m", "\033[0;35m",
          "\033[0;36m", "\033[0;37m", "\033[0;30m", "\033[0;31m", "\033[0;33m", "\033[0;34m"]
fonts = ["\033[1m", "\033[2m", "\033[3m", "\033[4m", "\033[5m"]
end_code = "\033[00m"




def login(username:str, password:str) -> bool:
    """This function receives a username and a password and returns 'ACCESS GRANTED'
    if the username is in the database and the password is correct, otherwise returns 'ACCESS DENIED'"""

    with open("db.csv", "r") as file:
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

user = input('Please enter your username: ')
password = input('Please enter your password: ')
test = login(password=password,username=user)
print(test)




welcome_msg = "Crypto Wallet".center(50, "=")
prompt_msg = "Please enter an option [1-5]: "

print(f"{colors[7]}{fonts[3]}{welcome_msg}{end_code}")
print("Options".center(50))

menu = """1. View Wallet Balance
2. Deposit or Withdraw Funds
3. Create and view transaction history
4. View Basic Description of the Cryptocurrency
5. Exit
"""
print(menu)
def Main():
    option = validate_int_input(prompt_msg)
    while option > 5 or option < 1:
        option = validate_int_input(f"{colors[1]}Invalid option.{prompt_msg}{end_code}")

# Option 2: Create a transaction (Enter, Withdraw, Record)
    if option == 2:
        transmenu = """1. Deposit
2. Withdraw"""
        print(transmenu)
        transmenu = validate_int_input('Please enter an option [1-2]: ')
        while transmenu > 2 or option < 1:
            transmenu = validate_int_input(f"{colors[1]}Invalid option. Please enter an option [1-2]: {end_code}")

        if transmenu == 1:
            with open("balance.csv", "a") as file:
                deposit = input("How much MKR would you like to deposit?: (ex. 10): ")
                file.write(f'{deposit}\n')
                print(f"{colors[2]}{fonts[0]}You have deposited {deposit}MKR into your wallet.{end_code}")

        if transmenu == 2:
            with open("withdraw.csv", "a") as file:
                withdraw = input("How much MKR would you like to withdraw?: (ex. 10): ")
                file.write(f'{withdraw}\n')
                print(f"{colors[2]}{fonts[0]}You have withdrawn {withdraw}MKR from your wallet.{end_code}")

# Option 1: Show current wallet balance
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
        print(f"{colors[7]}You have a current balance of {colors[2]}{total}MKR{end_code}, which is worth {colors[2]}${converted} USD{end_code}{end_code}")

# Option 3: Create or View Transaction History
    if option == 3:
        cvmenu = '''1. Create a transaction
2. View transaction history'''
        print(cvmenu)

        cvmenu = validate_int_input('Please enter an option [1-2]: ')
        while cvmenu > 2 or option < 1:
            cvmenu = validate_int_input(f"{colors[1]}Invalid option. Please enter an option [1-2]: {end_code}")

# cvmenu option 1: Create a transaction
        if cvmenu == 1:
            expensemenu = '''Please choose what type of expense your transaction is:
1. Food
2. Daily
3. Rent
4. Travel
5. Other'''
            print(expensemenu)
            expensemenu = validate_int_input('Please enter an option [1-5]: ')
            cats = ["Food", "Daily", "Rent", "Travel", "Other"]
            if expensemenu in [1,2,3,4,5]:
                with open("sheet.csv", "a") as file:
                    day = input('Please type when you made this transaction: MM/DD/YYYY: ')
                    cost = input('Please type the cost of this transaction: ex. 10: ')
                    transaction = f"{day},{cats[expensemenu-1]},{cost}"
                    file.write(f'{transaction}\n')
                    print(f"{colors[2]}{fonts[0]}You have created a transaction for {cost}MKR for {cats[expensemenu - 1]} on {day}.{end_code}")

# cvmenu option 2: View transaction history
        if cvmenu == 2:

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


# Option 4: Information about your cryptocurrency Maker (MKR)
    if option == 4:
        print(f"{colors[7]}4. Information about your cryptocurrency Maker (MKR):{end_code}")
        info = '''Maker (MKR) is a smart contract platform built on the Ethereum blockchain that aims to solve 
volatility issues for the crypto market. It is the basis for a new-generation blockchain-based banking system 
that allows for faster and simpler international payments and peer-to-peer transactions. Maker aims to unlock 
the potential of decentralized finance by building an inclusive platform for economic empowerment that gives 
everyone equal access to the global financial marketplace. 
'''
        print(f"{colors[9]}{info}{end_code}")

# Option 5: Exit
    if option == 5:
        print(f"{colors[6]}Exiting...{end_code}")
        print(f"{colors[7]}{fonts[3]}See you soon!{end_code}".center(50, "="))
        exit()



# Return to main menu
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
            print(f"{colors[7]}{fonts[3]}{thankyoumsg}{end_code}")
            exit()
Main()
```


