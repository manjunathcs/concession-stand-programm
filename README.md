🛒 Simple Food Ordering System
A simple Python program that allows users to order food items from a predefined menu, add them to a cart, and calculate the total bill.

📌 Features
Displays a menu with food items and prices
Allows users to add items to a cart
Calculates and displays the total bill
Handles invalid inputs gracefully
📜 How to Use
Run the script in a Python environment.
The menu will be displayed with food items and their prices.
Enter the food item name to add it to the cart.
Type q to quit and display the total bill.
🖥️ Example Output
yaml
Copy
Edit
-----------MENU-------------
pizza     : Rs100.00
briyani   : Rs200.00
chocolate : Rs150.00
popcorn   : Rs80.00
Enter the item (q to quit): pizza
Enter the item (q to quit): briyani
Enter the item (q to quit): chocolate
Enter the item (q to quit): q

Items in cart:
pizza briyani chocolate 
Total bill is: Rs 450.00
🛠 Requirements
Python 3.x
📜 Code
python
Copy
Edit
menu = {"pizza": 100,
        "briyani": 200,
        "chocolate": 150,
        "popcorn": 80}

cart = []
total = 0

print("-----------MENU-------------")

for key, values in menu.items():
    print(f"{key:10}: Rs{values:.2f}")

while True:
    food = input("Enter the item (q to quit): ").lower()
    if food == "q":
        break
    elif food in menu:
        cart.append(food)
    else:
        print("Item not found in menu, please try again.")

print("\nItems in cart:")
for food in cart:
    total += menu[food]
    print(food, end=" ")

print(f"\nTotal bill is: Rs {total:.2f}")
📌 License
This project is licensed under the MIT License.

