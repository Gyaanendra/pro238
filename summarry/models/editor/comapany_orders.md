## CompanyOrders Model

The `CompanyOrders` model represents orders placed by customers in a company. It defines the table structure and provides a method for creating order records.

### Model Explanation:

- Table Name: `company_orders`
- Columns:
  - `id`: Integer column, primary key.
  - `date`: DateTime column, stores the date of the order.
  - `customer_id`: Integer column, foreign key referencing the `id` column in the `customers` table.
  - `total_amount`: Float column, stores the total amount of the order.
  - `order_number`: Integer column, stores the order number.
- Relationships:
  - `customer`: Many-to-one relationship with the `Customer` model. Represents the customer who placed the order.

### Methods:

- `create(id, date, customer_id, total_amount, order_number)`: Static method that creates a new order record in the database. It takes the `id`, `date`, `customer_id`, `total_amount`, and `order_number` as parameters, creates a new `CompanyOrders` object with the provided details, adds it to the session, and commits the transaction to the database.

This model represents order information in a company and provides a method for creating order records. It also establishes a relationship with the `Customer` model to associate the orders with the corresponding customer.
