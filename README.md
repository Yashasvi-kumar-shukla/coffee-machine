# coffee-machine
#coffee machine emulator
water = 500
milk = 500
coffee = 100
money = 0
while True:
    n = input("What would you like?(espresso/latte/cappuccino):")
    if n == 'report':
        print("Water: ", water)
        print("Milk: ", milk)
        print("coffee: ", coffee)
        print("Money: ", money)
    elif n == 'latte':
        if water >= 200 and milk >= 150 and coffee >= 24:
            coin = float(input("enter the money for coffee:"))
            if coin == 2.5:
                water -= 200
                milk -= 150
                coffee -= 24
                money += coin
                print("cost of latte is 2.5 here enjoy your latte")
            elif coin >= 2.5:
                water -= 200
                milk -= 150
                coffee -= 24
                money += 2.5
                print("here is your ", coin - 2.5, " change for latte ")
            else:
                print("insufficient money, money refunded")
        else:
            print("resource unavailable")
    elif n == 'espresso':
        if water >= 50 and coffee >= 18:
            coin = float(input("enter the money for coffee:"))
            if coin == 1.5:
                water -= 50
                coffee -= 18
                money += coin
                print("cost of latte is 2.5 here enjoy your latte")
            elif coin >= 1.5:
                water -= 50
                coffee -= 18
                money += 1.5
                print("here is your ", coin - 1.5, " change for latte ")
            else:
                print("insufficient money, money refunded")
        else:
            print("resource unavailable")
    elif n == 'cappuccino':
        if water >= 250 and milk >= 100 and coffee >= 24:
            coin = float(input("enter the money for coffee:"))
            if coin == 3.0:
                water -= 250
                milk -= 100
                coffee -= 24
                money += coin
                print("cost of latte is 3.0 here enjoy your latte")
            elif coin >= 3.0:
                water -= 250
                milk -= 100
                coffee -= 24
                money += 3.0
                print("here is your ", coin - 3.0, " change for latte ")
            else:
                print("insufficient money, money refunded")
        else:
            print("resource unavailable")
    elif n == 'power off':
        exit()
        
