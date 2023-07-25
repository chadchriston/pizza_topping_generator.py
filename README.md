# pizza_topping_generator.py
import random

def generate_pizza_toppings(num_toppings=3):
    toppings_list = [
        'Pepperoni', 'Mushrooms', 'Onions', 'Sausage', 'Bacon',
        'Extra cheese', 'Black olives', 'Green peppers', 'Pineapple',
        'Spinach', 'Tomatoes', 'Ham', 'Jalapenos', 'Bell peppers',
    ]

    # Make sure the number of toppings doesn't exceed the available options
    num_toppings = min(num_toppings, len(toppings_list))

    # Randomly select toppings
    selected_toppings = random.sample(toppings_list, num_toppings)
    return selected_toppings

def main():
    num_toppings = int(input("How many toppings do you want on your pizza? "))
    pizza_toppings = generate_pizza_toppings(num_toppings)

    print("Your pizza with", num_toppings, "toppings:")
    for i, topping in enumerate(pizza_toppings, 1):
        print(f"{i}. {topping}")

if __name__ == "__main__":
    main()

