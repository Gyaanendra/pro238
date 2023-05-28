## Orders Model

The `Orders` model represents the orders placed by users in the application. It defines the table structure and provides methods for creating and updating order records.

### Model Explanation:

- Table Name: `orders`
- Columns:
  - `id`: Integer column, primary key.
  - `guid`: String column, stores a unique identifier for the order (UUID).
  - `user_id`: Integer column, foreign key referencing the `id` column of the `users` table.
  - `product_id`: Integer column, foreign key referencing the `id` column of the `products` table.
  - `product`: Relationship with the `Products` model, representing the associated product for the order.
  - `quantity`: Integer column, stores the quantity of the ordered product.
  - `address_id`: Integer column, foreign key referencing the `id` column of the `address` table.
  - `address`: Relationship with the `Address` model, representing the associated address for the order.
  - `amount`: Float column, stores the total amount of the order.

### Methods:

- `create(user_id, product_id, quantity, address_id, amount)`: Static method that creates a new order record in the database. It takes the `user_id`, `product_id`, `quantity`, `address_id`, and `amount` as parameters, generates a unique `guid` using UUID, creates a new `Orders` object with the provided details, adds it to the session, and commits the transaction to the database.
- `update(**details_dict)`: Method that updates the order record with the provided details. It takes a dictionary of attribute-value pairs as input, sets the corresponding attributes of the `Orders` object, and commits the changes to the database.

This model represents the orders placed by users and provides methods for creating and updating order records in the database.
