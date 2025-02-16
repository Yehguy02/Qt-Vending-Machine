# Qt-Vending-Machine
## Welcome to Qt vending machine project
  This is a project where it will simulates the vending machine that you can buy stuff inside the machine, as well as manipulate the machine if you have access rights.

## Guides to using Qt vending machine
### Machine basics
  The machine consist of 3 main parts; the item groups, the user tab, and the admin tab. There are an additional input / output text box for various reason
    The input text box are used in entering admin mode. 
    The output text box are used in returning actionss / error that occured during usage.

### The item group part
  It is where all the items are display. There is an item's name, item's price, and item's amount in the machine. If the item is out of stock, the amount will display None. The button below the amount is a select button which will select the item and display it in purchasing group, which will be explained next.

### The user part
  This is where most of purchasing action will take place. It starts right after selecting an item of choice, then there is a button to confirm that you would like to buy the items. You CANNOT undo the selection once confirmed. After confirmed, the item group will be disable and payment group will be enable. In the purchase group you can choose to pay with 100 Baht bills, 20 Baht bills, 10 Baht coins, 5 Baht coins, or 1 Baht coins. When select any of those, it will display the total payment that you've paid, the remainging payment that you still need to pay before purchasing item, and a change which will show how much the machine will return. If insert enough money, you can no longer able to insert more money. When pressing purchase button, the item amount will be decrease, change box will be decrease depends on how much change needs to be given, and the money inside collection box will be increase. These actions are all recorded in data base file.

  Do note that these actions are posible if the machines met a certain conditions. 
    First, each bills / coins in change box mustn't be empty. 
    Second, each bills / coins slot in collection box mustn't be full, in this case no more than 200.
    Third, the items must be available more than half.
  If any of these conditions aren't met, the machine will not operate.

### The admin part
  With access rights, you can access / change the content of the vending machine freely. First, You can restock / change items in the item group using the restock tab. The only conditions is that slot No., price, and amount must entered with positive integer number, if not then the machine will yeild error. Next, you can refill the change box by entering an amount you want to refill. Again, the conditions are entering positive integer for all the slots. Lastly, you can collect money in the machine by using collect money button.
  
