# Customer Notes and Requirements
Hello, Team 9! It is a pleasure to collaborate with your engineering team to assist my café in developing an application that will allow clients to place pick-up orders from our menu.

This software for our menu needs to allow customers to clearly view our items, select their choices, and easily/securely make their purchases. Other things that I require, or desire, might not be included in this initial draft. As you read this, you will quickly realize what I simply cannot function without in the initial edition. If you're unsure, please reach out and let me know.

Below are the cafe items we will have for sale.

### Menu Options

**Speciality Drinks:**

1.	Lavender Honey Latte (5)
A soothing blend of espresso, steamed milk, lavender syrup, and a drizzle of honey.
2.	Matcha Coconut Bliss (5)
Creamy matcha green tea mixed with coconut milk and a hint of vanilla.
3.	Salted Caramel Mocha (5)
Rich espresso with chocolate, salted caramel sauce, and whipped cream.
4.	Berry Hibiscus Cooler (5)
A refreshing iced tea with hibiscus, mixed berries, and a splash of lemon.
________________________________________
**One-of-a-Kind Pastries:**
1.	Lemon Blueberry Cheesecake Danish (10)
Flaky pastry filled with lemon cheesecake and topped with fresh blueberries.
2.	Salted Dark Chocolate Croissant (10)
Buttery croissant with a gooey dark chocolate filling and a sprinkle of sea salt.
3.	Matcha White Chocolate Scone (10)
A tender scone infused with matcha and studded with white chocolate chips.
4.	Pistachio Cardamom Roll (10)
Soft, sweet roll with a pistachio-cardamom filling and a drizzle of icing.


## User Registration and Login

Users (costumers) must be able to log in to the system.

There must be an admin user type for (employees) to have access and be able to log in and run sales reports. Admins cannot self-register, someone whose already admin has to give that person the employee access. A simple user interface for this would be great, but a manual process is acceptable for Version 1.

*All users must have a unique username and a 6-character (minimum) password link with their emails for notifications.*

## Main Screen (Menu Display)

-	After logging in, the user must see a list of all available menu items, sorted by highest price to lowest price.

-	Users cannot see items that are out of stock.

###	Each item must include:

-	Short name of item

-	1 or 2 Pictures

- Price (formatted in US dollars with a $ sign, commas, and decimal points)

-	Brief description

-	Button to add the item to an order

-	Users can add multiple items to the order.

-	Users should be able to search through the menu by typing in a search box. The system will match the words to the item’s name.

### An example of an item for sale might look like this:

-	Name: Salted Caramel Mocha,

-	[Picture of item is inserted here]

-	Price: $5

-	Description: "Rich espresso with chocolate, salted caramel sauce, and whipped cream."

### Order Creation and Checkout

-	Users can click a place order or check out button to finalize the order.

-	Users cannot click place order or check out button if the order is empty.

###	After clicking Checkout, Our users must see:

-	A list of items in the order.

-	A subtotal cost in US dollars.

-	They should be able to remove items from the order.

*If all items are removed, the user is automatically returned to the main screen.*

### From the order page, users can:

- Click the Confirm Order button to finalize the transaction.

-	Return to the menu to add more items.

## Order Confirmation
### When the Confirm Order button is clicked, users must see:
-	A list of items in the order (name and price only).
-	Subtotal
-	Tax (6% of the subtotal)
-	Total cost
*Example: If 3 items in cart make a total of $20. After the taxes are added the order should total in $21.20.*

### Users can:
-	Click Complete Order to finalize the transaction.
-	Back up to the order page to make changes.
-	Return to the main menu.

## Receipt Generation
### After clicking Complete Order, the system must generate a receipt that includes:
-	List of ordered items (name and price).
-	Subtotal, tax, and total cost.
-	Print the receipt for the customer.
-	Users can click OK to return to the main menu.
*At this point, the order is complete, and the items are removed from inventory.*

## Admin Features

### Admins must be able to:
-	Run a sales report showing everything sold and the total revenue. (Ideally, clicking on a sold item should show the related receipt)
-	Export the sales report to CSV for analysis in tools like Excel.
-	Add new menu items to the system.
  
*Preferred: A page where admins can enter item details (name, price, description, picture) and add it to the database.*

*Alternative: Manual entry into the database (with clear instructions for non-technical admins).*

### High-Fidelity Mockup
-	Before coding starts, I need a high-fidelity mockup of the screens and application flow.
-	This will help me visualize how the application will look and function when completed.
## Additional Notes
-	Prices must be stored in a decimal/currency format (base-10, not floating point).
-	The application must be user-friendly and visually appealing to enhance the staff and customer experience.
