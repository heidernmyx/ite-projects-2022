print ("""

\t\t======= Welcome to Gaisano Mall ========
--------------------------------------------------------------------------------
""")
from datetime import datetime
#stocks
tissue = 10
apple = 20
yellow_pad = 10
marker = 15
koolers = 15
total_price = 0

product1=0
product2=0
product3=0
product4=0
product5=0

quantity1=0
quantity2=0
quantity3=0
quantity4=0
quantity5=0

total_price1=0
total_price2=0
total_price3=0
total_price4=0
total_price5=0

item = input(f"""

Select your order:
Product		              Price		   Stocks Available
1. Tissue                 \t20                       {tissue}
2. Apple                  \t15                       {apple}
3. Yellow pad             \t25                       {yellow_pad}
4. White board marker     \t25                       {marker}
5. Koolers (Mango Flav.)  \t15                       {koolers}

Enter your order: """)

while item != "1" and item != "2" and item != "3" and item != "4" and item != "5":
    print ("Invalid input, Please try again")
    item = input(f"""
    
Select your order:
Product		              Price		   Stocks Available
1. Tissue                 \t20                       {tissue}
2. Apple                  \t15                       {apple}
3. Yellow pad             \t25                       {yellow_pad}
4. White board marker     \t25                       {marker}
5. Koolers (Mango Flav.)  \t15                       {koolers}

Enter your order: """)


while item == "1" or item == "2" or item == "3" or item == "4" or item == "5":
    if item == "1" and tissue > 0:
        product1=1
        quantity_purchase= int(input("Enter quantity: "))
        while quantity_purchase > tissue:
            print ("Quantity input exceeded current stock, Please try again")
            quantity_purchase = int(input("Enter quantity: "))
        tissue = tissue - quantity_purchase
        quantity1 += quantity_purchase
        price = quantity1 * 20
        total_price1 = total_price + price

       
       
    elif item == "2" and apple > 0:
        product2=1
        quantity_purchase = int(input("Enter quantity: "))
        while quantity_purchase > apple:
            print ("Quantity input exceeded current stock, Please try again")
            quantity_purchase = int(input("Enter quantity: "))
        apple = apple - quantity_purchase
        quantity2 += quantity_purchase
        price = quantity2 * 15
        total_price2 = total_price + price

     
      
    elif item == "3" and yellow_pad > 0:
        product3=1
        quantity_purchase = int(input("Enter quantity: "))
        while quantity_purchase > yellow_pad:
            print ("Quantity input exceeded current stock, Please try again")
            quantity_purchase = int(input("Enter quantity: "))
        yellow_pad = yellow_pad - quantity_purchase
        quantity3 += quantity_purchase
        price = quantity3 * 25
        total_price3 = total_price + price

  
        
    elif item == "4" and marker > 0:
        product4=1
        quantity_purchase = int(input("Enter quantity: "))
        while quantity_purchase > marker:
            print ("Quantity input exceeded current stock, Please try again")
            quantity_purchase = int(input("Enter quantity: "))
        marker = marker - quantity_purchase
        quantity4 += quantity_purchase
        price = quantity4 * 25
        total_price4 = total_price + price

      
        
    elif item == "5" and koolers > 0:
        product5=1
        quantity_purchase = int(input("Enter quantity: "))
        while quantity_purchase > koolers:
            print ("Quantity input exceeded current stock, Please try again")
            quantity_purchase = int(input("Enter quantity: "))
        koolers = koolers - quantity_purchase
        quantity5 += quantity_purchase
        price = quantity5 * 15
        total_price5 = total_price + price
       
        print ("______________________________________________________________________________")
        
    elif tissue == 0 or apple == 0 or yellow_pad == 0 or marker == 0 or kooelers == 0:
        print ("Item out of stock,Selection of order terminated")
        
    AllTotal =total_price1 +total_price2 +total_price3+total_price4+ total_price5
    print ("\n\n\nCurrent Orders           Quantity          Price        Total")
    if product1==1:
            print (f"Tissue          \t    {quantity1} X      \t    20 \t\t {total_price1}")
    if product2==1:
            print (f"Apple          \t\t    {quantity2} X      \t    15 \t\t {total_price2}")    
    if product3==1:
            print (f"Yellow Pad      \t    {quantity3} X     \t    25 \t\t {total_price3}")
    if product4==1:
            print (f"White Board Marker          {quantity4} X     \t    25 \t\t {total_price4}")
    if product5==1:
            print (f"Koolers (Mango Flav.)       {quantity5} X   \t    15 \t\t {total_price5}")
    print (f"\n\nSubtotal: .............................................  {AllTotal}")
    
    if tissue == 0 and apple == 0 and yellow_pad == 0 and marker == 0 and koolers == 0:
        print (f"\n\nAMOUNT TO BE PAID: {AllTotal}")
        amount = int(input("Enter AMOUNT: "))
        
        while amount <AllTotal:
            print (f"\n\nInvalid !! Amount should be EQUAL or GREATER !!")
            amount = int(input("Enter AMOUNT: "))
        
        AllTotal =total_price1 +total_price2 +total_price3+total_price4+ total_price5
        import datetime
        now = datetime.datetime.now()
        print ("\n\n\n________________________________________________________________________________")
        print ("\n\t\t\t\t  GAISANO MALL\n")
        
        print ("--------------------------------Official Reciept--------------------------------")
        print (now.strftime("\tDate: %Y-%m-%d \n\t Time: %H:%M:%S"))
        print ("\n")
        print ("Orders\n")
        print ("Item        \t\tQuantity          Price          Total\n")
        if product1==1:
            print (f"Tissue        \t\t    {quantity1}      \t    20   \t   {total_price1}")
        if product2==1:
            print (f"Apple        \t\t    {quantity2}      \t    15   \t   {total_price2}")    
        if product3==1:
            print (f"Yellow Pad    \t\t    {quantity3}      \t    25    \t   {total_price3}")
        if product4==1:
            print (f"White Board Marker   \t    {quantity4}     \t    25   \t   {total_price4}")
        if product5==1:
            print (f"Koolers (Mango Flav.)  \t    {quantity5}         \t    15   \t   {total_price5}")
        print ("\n\n\n________________________________________________________________________________")
        Change = amount-AllTotal
        print (f"\nTOTAL: ...............................................     {AllTotal}")
        print (f"\nAMOUNT PAID: ..........................................    {amount}")
        print (f"\nCHANGE: ...............................................    {Change}")

        break
    
    
    order = input("\n\nOrder again? y/n: ").lower()
    
    
    while order != "y" and order != "n":
        order = input("\n\nOrder again? y/n: ").lower()
        
    if order == "y":
        item = input(f"""
        
        \n\nSelect your order
Product		             Price		        Stocks Available
1. Tissue                 20                       {tissue}
2. Apple                  15                       {apple}
3. Yellow pad             25                       {yellow_pad}
4. White Board Marker     25                       {marker}
5. Koolers (Mango Flav.)  15                       {koolers}

Enter your order: """)
        while item != "1" and item != "2" and item != "3" and item != "4" and item != "5":
            print ("Invalid input, Please try again")
            item = input(f"""
        
        \n\nSelect your order
Product		             Price		        Stocks Available
1. Tissue                 20                       {tissue}
2. Apple                  15                       {apple}
3. Yellow pad             25                       {yellow_pad}
4. White Board Marker     25                       {marker}
5. Koolers (Mango Flav.)  15                       {koolers}

Enter your order: """)
    

#order summary
    elif order == "n":
        print (f"\n\nAMOUNT TO BE PAID: {AllTotal}")
        amount = int(input("Enter AMOUNT: "))
        
        while amount <AllTotal:
            print (f"\n\nInvalid !! Amount should be EQUAL or GREATER !!")
            amount = int(input("Enter AMOUNT: "))
        
        AllTotal =total_price1 +total_price2 +total_price3+total_price4+ total_price5
        import datetime
        now = datetime.datetime.now()
        print ("\n\n\n________________________________________________________________________________")
        print ("\n\t\t\t\t  GAISANO MALL\n")
        
        print ("--------------------------------Official Reciept--------------------------------")
        print (now.strftime("\tDate: %Y-%m-%d \n\t Time: %H:%M:%S"))
        print ("\n")
        print ("Orders\n")
        print ("Item        \t\tQuantity          Price          Total\n")
        if product1==1:
            print (f"Tissue        \t\t    {quantity1}      \t    20   \t   {total_price1}")
        if product2==1:
            print (f"Apple        \t\t    {quantity2}      \t    15   \t   {total_price2}")    
        if product3==1:
            print (f"Yellow Pad    \t\t    {quantity3}      \t    25    \t   {total_price3}")
        if product4==1:
            print (f"White Board Marker   \t    {quantity4}     \t    25   \t   {total_price4}")
        if product5==1:
            print (f"Koolers (Mango Flav.)  \t    {quantity5}         \t    15   \t   {total_price5}")
        print ("\n\n\n________________________________________________________________________________")
        Change = amount-AllTotal
        print (f"\nTOTAL: ...............................................     {AllTotal}")
        print (f"\nAMOUNT PAID: ..........................................    {amount}")
        print (f"\nCHANGE: ...............................................    {Change}")

        break
