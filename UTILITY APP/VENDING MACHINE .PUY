# Item names
names = {
    '010': 'Pepsi',
    '012': 'Cake',
    '013': 'Juice',
    '014': 'KitKat',
    '015': 'Water',
    '016': 'Coffee',
    '017': 'Tea'
}

# Price dictionary for items
prices = {
    '010': 2,     # Pepsi price
    '012': 1,     # Cake price
    '013': 1.50,  # Juice price
    '014': 3.50,  # KitKat price
    '015': 1,     # Water price
    '016': 2,     # Coffee price
    '017': 1      # Tea price
}

# Initialize stock for each item
stock = {
    '010': 3,  # Pepsi
    '012': 5,   # Cake
    '013': 7,   # Juice
    '014': 4,   # KitKat
    '015': 20,  # Water
    '016': 8,   # Coffee
    '017': 15   # Tea
}

print("=======================================")
print("WELCOME TO THE VENDING MACHINE!!")
print("=======================================")
print("Item\tPrice\tCode")
for code, name in names.items():
    print(f"{name}\t{prices[code]} AED\t{code}")

while True:
    code = input("-----------------------------\nEnter the product code:\n")

    if code in stock:
        # Check if the item is in stock
        if stock[code] > 0:
            print(f"You have chosen {names[code]}!")
            price = prices[code]

            #  payment input
            while True:
                amount_input = input(f"Pay the amount ({price} AED):\n")
                try:
                    amount_paid = float(amount_input)
                    break  # Exit loop if input is valid
                except ValueError:
                    print("Invalid input. Please enter a valid number.")

            # Handle payment logic
            if amount_paid > price:
                print(f"Take your change ({amount_paid - price} AED) and your {names[code]}.")
                stock[code] -= 1  # Decrease stock
            elif amount_paid < price:
                print("Not enough money. Amount refunded.")
            else:
                print(f"Here is your {names[code]}. Enjoy!")
                stock[code] -= 1  # Decrease stock

            print(f"Remaining stock of {names[code]}: {stock[code]}")  # Show remaining stock
        else:
            print(f"Sorry, {names[code]} is out of stock.")
    else:
        print("Invalid code. Please try again.")

    # Check if the user wants to buy something more
    continue_shopping = input("-----------------------------\nBuy something more? (yes/no):\n").lower()
    if continue_shopping == 'no':
        print("=======================================")
        print("THANK YOU FOR USING THE VENDING MACHINE!!")
        print("=======================================")
        break
