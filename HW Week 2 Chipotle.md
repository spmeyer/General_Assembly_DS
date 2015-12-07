# Steve Meyer GA Week 2 Homework Chipotle.tsv


##1. Head, Tail, and Description
### head chipotle.tsv
Steven-Meyers-MacBook-Pro:data spmeyer$ head chipotle.tsv
order_id	quantity	item_name	choice_description	item_price
1	1	Chips and Fresh Tomato Salsa	NULL	$2.39 
1	1	Izze	[Clementine]	$3.39 
1	1	Nantucket Nectar	[Apple]	$3.39 
1	1	Chips and Tomatillo-Green Chili Salsa	NULL	$2.39 
2	2	Chicken Bowl	[Tomatillo-Red Chili Salsa (Hot), [Black Beans, Rice, Cheese, Sour Cream]]	$16.98 
3	1	Chicken Bowl	[Fresh Tomato Salsa (Mild), [Rice, Cheese, Sour Cream, Guacamole, Lettuce]]	$10.98 
3	1	Side of Chips	NULL	$1.69 
4	1	Steak Burrito	[Tomatillo Red Chili Salsa, [Fajita Vegetables, Black Beans, Pinto Beans, Cheese, Sour Cream, Guacamole, Lettuce]]	$11.75 
4	1	Steak Soft Tacos	[Tomatillo Green Chili Salsa, [Pinto Beans, Cheese, Sour Cream, Lettuce]]	$9.25 

### tail.chipotle.tsv
Steven-Meyers-MacBook-Pro:data spmeyer$ tail chipotle.tsv
1831	1	Carnitas Bowl	[Fresh Tomato Salsa, [Fajita Vegetables, Rice, Black Beans, Cheese, Sour Cream, Lettuce]]	$9.25 
1831	1	Chips	NULL	$2.15 
1831	1	Bottled Water	NULL	$1.50 
1832	1	Chicken Soft Tacos	[Fresh Tomato Salsa, [Rice, Cheese, Sour Cream]]	$8.75 
1832	1	Chips and Guacamole	NULL	$4.45 
1833	1	Steak Burrito	[Fresh Tomato Salsa, [Rice, Black Beans, Sour Cream, Cheese, Lettuce, Guacamole]]	$11.75 
1833	1	Steak Burrito	[Fresh Tomato Salsa, [Rice, Sour Cream, Cheese, Lettuce, Guacamole]]	$11.75 
1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Guacamole, Lettuce]]	$11.25 
1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita Vegetables, Lettuce]]	$8.75 
1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Lettuce]]	$8.75 

### What is this data?  Explain columns and rows.
I think this data is a record of Chipotle purchases.
The columns are: 
* order_id:  This is the order number.
     For example, order_id = 1 had the first 4 rows, that is, 4 menu item types were ordered; 
                  order_id = 2 only had 1 row, that is, 1 menu item type was ordered.
* quantity:  This is how many of a certain menu item type were ordered.  
     For example, order_id = 3 ordered just 1 "Side of Chips"
                  order_id = 2 ordered 2 "Chicken Bowls"
* item_name: This column tells us the name of the item ordered such as "Chips" or "Bottled Water"	
* choice_description: This columns tells how the customer wanted their item customized.  
     For example, order_id = 1 ordered an item name = "Izze" and wanted that had a choice_description = "Clementine", which is the flavor in this case.
     Likewise, order_id = 1834 ordered 3 Chicken Salad Vowls, but each had a different list of items in those bowls - that is, this first listed gaucamole (among other things) and third listed pinto beans.
* item_price:  Simply the price of the item purchased.


##2. There appear to be 1834 orders.
Steven-Meyers-MacBook-Pro:data spmeyer$ tail -n1 chipotle.tsv
1834	1	Chicken Salad Bowl	[Fresh Tomato Salsa, [Fajita Vegetables, Pinto Beans, Lettuce]]	$8.75 


##3. There are 4,623 lines in this file.
Steven-Meyers-MacBook-Pro:data spmeyer$ wc -l chipotle.tsv
    4623 chipotle.tsv


##4. At first look Chicken Burritos appear to be more popular than Steak Burritos, but it is worth noting I did get a quantity count for each item.
Steven-Meyers-MacBook-Pro:data spmeyer$ cat chipotle.tsv | grep "Steak Burrito" | wc -l
     368
Steven-Meyers-MacBook-Pro:data spmeyer$ cat chipotle.tsv | grep "Chicken Burrito" | wc -l
     553
     

##5. At first look, in Chicago Burritos Black Beans appear to be more popular than Pinto Beans
Steven-Meyers-MacBook-Pro:data spmeyer$ cat chipotle.tsv | grep "Chicken Burrito" | grep "Black Beans" | wc -l
     282
Steven-Meyers-MacBook-Pro:data spmeyer$ cat chipotle.tsv | grep "Chicken Burrito" | grep "Pinto Beans" | wc -l
     105
     

##6. Find all files in repo ending with .csv or .tsv with one command
Steven-Meyers-MacBook-Pro:DAT-DC-10 spmeyer$ find . -type f -name "*.*sv"
./data/airlines.csv
./data/bank-additional.csv
./data/bikeshare.csv
./data/chipotle.tsv
./data/drinks.csv
./data/hitters.csv
./data/imdb_1000.csv
./data/sms.tsv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.csv


##7.  I found approximately 213 occurances of the word "dictionary" across all the files in the DC-DAT-10 repo.
Steven-Meyers-MacBook-Pro:DAT-DC-10 spmeyer$ find . "*ictionary" | wc -l
find: *ictionary: No such file or directory
     213


