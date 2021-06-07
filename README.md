# secret-auction-program
project2


bids={}
bidding=False

def func(bidding_record):
    highest_bid=0
    winner=" "
    for i in bidding_record:
        bidding_amout=bidding_record[i]
        if bidding_amout > highest_bid:
           highest_bid=bidding_amout
           winner=i
    print(f"the winner is {winner},with pricee{ highest_bid}")
while not bidding:
    name = input("ask user name: ")
    price =int(input("ask for their bid:"))
    bids[name] = price
    should_continue=input("are there any ohter bidder ? yes or no")
    if should_continue=="no":
        bidding=True
        func(bids)
    elif should_continue=="yes":
        bidding=False
