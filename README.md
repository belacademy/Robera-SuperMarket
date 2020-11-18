# Robera-SuperMarket(RSM)

| Smallest eCommerce proof of concept

## RSM platform has the following structure

* **Category**: a grouping of product

* **Product**:  an item that is ready to be sold

* **Inventory**: a tracking mechanism to identify the replenishing status

* **Supplier**: a person/organization providing inventory

* **Customer**: a potential buyer

* **User**: a model to identify Customer or Supplier

* **Order**: a tracking mechanism to identify buyer (customer) and good/item sold (product)

* **ShoppingCart**: a tracking mechanism of what the customer is going to buy

* **Payment**: a fullfilment tracking mechanism to track when the order is paid, what payment method used etc

## RSM - Relationships

***Category**     has_many products*
***Product**      belongs_to_many categories*
***Product**      has_many inventories*
***Product**      belongs_to supplier*
***Product**      belongs_to many shopping_carts*
***Inventory**    belongs_to product*
***Inventory**    belongs_to product*
***Suplier**      has_many products*
***Supplier**     has_many inventories*
***Supplier**     belongs_to user*
***Customer**     has_many orders*
***Customer**     belongs_to user*
***Customer**     has_one shopping_cart*
***Order**        belongs_to customer*
***Order**        has_one shopping_cart*
***ShoppingCart** belongs_to customer*
***ShoppingCart** has_many products*
***ShoppingCart** has_one order*
***User**         has_one customer*
***User**         has_one supplier*

## RSM - API endpoints

