ticket_price = 10
tickets_remaining = 100
SERVICE_CHARGE = 2


def calculate_price(ticketprice, userticketwant, SERVICE_CHARGE):
    return ticketprice * userticketwant + SERVICE_CHARGE


while tickets_remaining >= 1:
    print("There are {} tickets remaining".format(tickets_remaining))

    name = input("What's your name? ")
    try:
        userTicketWant = int(input("Hi {}! How many tickets would you like? ".format(name.capitalize())))
        totalPrice = calculate_price(ticket_price, userTicketWant, SERVICE_CHARGE)
        if userTicketWant > tickets_remaining:
            raise ValueError("Invalid amount of tickets")
    except ValueError as Err:
        print(f"On no! We run into a issue [{Err}]. Please try again.")
    else:
        print("Your amount due for the ticket was ${} because of the service charge of ${}".format(totalPrice, SERVICE_CHARGE))

        ansUser = input("Do you want to proceed now? Y/N: ")
        if ansUser.upper() == 'Y':
            print("SOLD!")
            tickets_remaining -= userTicketWant
        else:
            print("Thank you {}".format(name.capitalize()))
print("Tickets are sold out.")
