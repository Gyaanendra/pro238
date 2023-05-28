## OrderItems Model

The `OrderItems` model represents items included in an order. It defines the table structure and provides a method for creating order item records.

### Model Explanation:

- Table Name: `order_items`
- Columns:
  - `id`: Integer column, primary key.
  - `order_id`: Integer column, foreign key referencing the `id` column of the `company_orders` table.
  - `product_id`: Integer column, foreign key referencing the `id` column of the `company_products` table.
  - `unit_price`: Float column, stores the unit price of the ordered item.
  - `quantity`: Integer column, stores the quantity of the ordered item.

### Methods:

- `create(id, order_id, product_id, unit_price, quantity)`: Static method that creates a new order item record in the database. It takes the `id`, `order_id`, `product_id`, `unit_price`, and `quantity` as parameters, creates a new `OrderItems` object with the provided details, adds it to the session, and commits the transaction to the database.

This model represents the items included in an order and provides a method for creating order item records in the database. It captures details such as the order ID, product ID, unit price, and quantity of each ordered item.
