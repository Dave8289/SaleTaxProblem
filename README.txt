Basic sales tax is applicable at a rate of 10% on all goods, except books, food, and medical products that are exempt. 
Import duty is an additional sales tax applicable on all imported goods at a rate of 5%, with no exemptions.

When I purchase items I receive a receipt which lists the name of all the items and their price (including tax), 
finishing with the total cost of the items, and the total amounts of sales taxes paid. The rounding rules for sales tax are that for a tax rate
of n%, a shelf price of p contains (np/100 rounded up to the nearest 0.05) amount of sales tax.

Write an application that prints out the receipt details for these shopping baskets.

INPUT:
Input 1:

1 book at 12.49
1 music CD at 14.99
1 chocolate bar at 0.85

Input 2:

1 imported box of chocolates at 10.00
1 imported bottle of perfume at 47.50

Input 3:

1 imported bottle of perfume at 27.99
1 bottle of perfume at 18.99
1 packet of headache pills at 9.75
1 box of imported chocolates at 11.25

OUTPUT
Output 1:

1 book : 12.49
1 music CD: 16.49
1 chocolate bar: 0.85
Sales Taxes: 1.50
Total: 29.83

Output 2:

1 imported box of chocolates: 10.50
1 imported bottle of perfume: 54.65
Sales Taxes: 7.65
Total: 65.15

Output 3:

1 imported bottle of perfume: 32.19
1 bottle of perfume: 20.89
1 packet of headache pills: 9.75
1 imported box of chocolates: 11.85
Sales Taxes: 6.70
Total: 74.68

Introduction
This project was developed by Davinder Kumar

How to Run
Compile the project into a jar, or load the .java files into your favorite IDE and run the main method found in the Main class.
Make sure that the input txt files are the root of the project directory. 

Input Files:
input1.txt
input2.txt
input3.txt

Assumptions
The input text file follows the following syntax:
   1 book at 12.49
   qty, name, "at", price
 
Product Quantity is a positive integer
Price is a positive number
Items to be excluded from the goods sales tax (10%) is included in a text file called exclusions.txt placed in the input folder.
Imported items have the word imported in them.

Here is a overview of the program

Main Class

	main()

Receipt Class

	ArrayList<Product> productsList
	double total
	double taxtotal

	Receipt()
	calculateTotals()
	setTotal()
	getTotal()
	setSalesTaxTotal()
	getSalesTaxTotal()
	containsItemFromArray()
	round()
	roundTwoDecimals()
	printReceipt()

  
enum ItemType

	BOOK
	MEDICAL
	FOOD
	OTHERS
	IMPORTED_BOOK
	IMPORTED_MEDICAL
	IMPORTED_FOOD
	IMPORTED_OTHERS
	isExempted
	isImported
	
	ItemType()
	isImported()
	isExempted()
	
Product Class

	String name
	float price
	ItemType type
	
	product()
	toString()
	getPrice()
	setPrice()
	getName()
	setName()
	isSalesTaxable()
	isImportTaxable()
	
	
Program Flow

The main method creates a receipt object
The receipt object creates Product objects which are created using the information from the input text file
These products are put into a list field of the receipt object
The receipt object can then calculate the sales tax and total 
The receipt object can print the output in a nice format

