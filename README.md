# ShoppingCartDemo-PHP
ShoppingCartDemo-PHP

Tables:

1. PRODUCTS TABLE:

CREATE TABLE IF NOT EXISTS `products` (
  `productID` int(11) NOT NULL AUTO_INCREMENT,
  `pname` varchar(30) NOT NULL,
  `rate` decimal(10,0) NOT NULL,
  `pimage` varchar(300) NOT NULL,
  PRIMARY KEY (`productID`)
)

2. CART TABLE:

CREATE TABLE IF NOT EXISTS `cart` (
  `recordID` int(11) NOT NULL AUTO_INCREMENT,
  `userID` int(11) NOT NULL,
  `sessionID` varchar(30) NOT NULL,
  `productID` int(11) NOT NULL,
  `quantity` int(11) NOT NULL,
  `amount` decimal(10,0) NOT NULL,
  PRIMARY KEY (`recordID`)
)

3. ORDERS TABLE:
CREATE TABLE IF NOT EXISTS `orders` (
  `orderID` int(11) NOT NULL AUTO_INCREMENT,
  `userID` int(11) NOT NULL,
  `TotalAmount` decimal(10,0) NOT NULL,
  `orderDate` date NOT NULL,
  PRIMARY KEY (`orderID`)
)

4. ORDER ITEMS TABLE:

CREATE TABLE IF NOT EXISTS `order_items` (
  `recordID` int(11) NOT NULL AUTO_INCREMENT,
  `orderID` int(11) NOT NULL,
  `productID` int(11) NOT NULL,
  `quantity` int(11) NOT NULL,
  PRIMARY KEY (`recordID`)
)
