# Zero-hunger-using-Python
# Zero Hunger - Food Donation System

donations = []

def donate_food():
    name = input("Enter donor name: ")
    food = input("Enter food item: ")
    quantity = input("Enter quantity: ")
    
    donations.append({
        "name": name,
        "food": food,
        "quantity": quantity
    })
    
    print("✅ Donation added successfully!\n")

def view_donations():
    if not donations:
        print("No donations available.\n")
    else:
        print("\n🍽️ Available Donations:")
        for d in donations:
            print(f"Donor: {d['name']}, Food: {d['food']}, Quantity: {d['quantity']}")
        print()

def main():
    while True:
        print("1. Donate Food")
        print("2. View Donations")
        print("3. Exit")
        
        choice = input("Enter choice: ")
        
        if choice == "1":
            donate_food()
        elif choice == "2":
            view_donations()
        elif choice == "3":
            print("Thank you for supporting Zero Hunger!")
            break
        else:
            print("Invalid choice!\n")

main()
