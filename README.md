# MySQL Workshop 2 - Basic Data Manipulation


## Workshop Contents

### Data Manipulation Statements

* [Insert](http://dev.mysql.com/doc/refman/5.7/en/insert.html)
* [Update](http://dev.mysql.com/doc/refman/5.7/en/update.html)
* [Delete](http://dev.mysql.com/doc/refman/5.7/en/delete.html)

### Data Manipulation Queries

* [Select](http://dev.mysql.com/doc/refman/5.7/en/select.html)
  * [Count](https://dev.mysql.com/doc/refman/5.7/en/counting-rows.html)

### Query Clauses

* [Limit](http://dev.mysql.com/doc/refman/5.7/en/limit-optimization.html)
* [Where](https://dev.mysql.com/doc/refman/5.7/en/where-optimizations.html)
  * [Logical And Operator](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_and)
  * [Logical Or Operator](https://dev.mysql.com/doc/refman/5.7/en/logical-operators.html#operator_or)
  * [Like Operator](https://dev.mysql.com/doc/refman/5.7/en/string-comparison-functions.html#operator_like)
  * [Between Operator](https://dev.mysql.com/doc/refman/5.7/en/comparison-operators.html#operator_between)

### Query Modifiers

* [Order By](http://dev.mysql.com/doc/internals/en/optimizer-order-by-clauses.html)
* [Group By](http://dev.mysql.com/doc/internals/en/optimizer-group-by-related-conditions.html)


### MySQL Batch Import
```
# Executing Statements from an External File
mysql> source <filename>
```

## Workshop Instructions

* Fork this repository
* Create a new Cloud9 Workspace
* For every exercise in this Workshop:
  * Create a new branch off from "master" named "exercise-n"
  * Create a new file named "exercise-n.txt", containing:
    * The SQL Statement used, when applicable
    * The SQL Statement results, when applicable
  * Create a pull request


### Exercise 1
* Insert one row into ```decodemtl_addressbook.Account```
* Insert one row into ```decodemtl_addressbook.AddressBook```
* Insert three rows into ```decodemtl_addressbook.Entry```

### Exercise 2
* Retrieve data from the previously inserted ```decodemtl_addressbook.Account``` row
* Retrieve data from the previously inserted ```decodemtl_addressbook.AddressBook``` row
* Retrieve data from the previously inserted ```decodemtl_addressbook.Entry``` rows

### Exercise 3
* Modify the ```decodemtl_addressbook.Account``` row
* Modify the ```decodemtl_addressbook.AddressBook``` row
* Modify the three ```decodemtl_addressbook.Entry``` rows using one query only

### Exercise 4
* Delete all data from ```decodemtl_addressbook.Entry``` without using a ```DELETE``` statement

### Exercise 5
* Delete ```decodemtl_addressbook.Account``` and all associated date

### Exercise 6
* Create database ```decodemtl_addressbook_import```
* Bulk import data from the source files into ```decodemtl_addressbook_import```:
  * data/import-account.sql
  * data/import-addressbook.sql
  * data/import-entry.sql

### Exercise 7
* What is the email of the Account identified by "63"?
* What are the names of the AdressBooks belonging to accountId "3"?
* On which date was the AddressBook titled "Lorem Foundation" created?

### Exercise 8
* How many Accounts exist?
* How many Address Books exist?
* How many Address Book Entries exist?

### Exercise 9
* How many Address Book Entries are listed as born before February 12th of 1982?
* How many Address Book Entries are listed as born on or after January 1st of 1965?
* Which Address Book Entry is listed as being the oldest of age?

### Exercise 10
* How many Address Book Entries are not listed as ```other```?
* How many Address Book Entries are listed as both ```home``` and ```work```?
* How many Address Book Entries are listed as ```phones```?

### Exercise 11
* Which Account owns the most Address Books?
* Which Address Book contains the most Entries?

### Exercise 12
* How many Address Book Entries have phones starting with area code ```3XX```?
* How many Address Book Entries have ```home``` phones not containing the digit ```5```?
* How many Address Book Entries are ```work``` phones starting with a country code?

### Exercise 13 (Workshop Challenge)
* Create a data model representing a Store with Inventory, Customers and Invoices
* This model should provide answers to the following questions:
  * What is the Store's income within a specific date range?
  * What is the Store's top selling Inventory product?
  * Which company produces the top selling Inventory product?
  * What is the top refunded Inventory product?
  * Which products should be taken out from the Store's Inventory?
  * Which companies should the Store stop selling products from?
  * What is the amount of Internal (Canadian) vs. External sales?
  * How many of a specific product remains in Inventory for a specific date?