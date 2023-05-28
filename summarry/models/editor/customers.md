## Customer Model

The `Customer` model represents a customer in the system. It defines the table structure and provides a method for creating customer records.

### Model Explanation:

- Table Name: `customers`
- Columns:
  - `id`: Integer column, primary key.
  - `first_name`: String column, stores the first name of the customer.
  - `last_name`: String column, stores the last name of the customer.
  - `city`: String column, stores the city of the customer.
  - `country`: String column, stores the country of the customer.
  - `phone`: String column, stores the phone number of the customer.

### Methods:

- `create(id, first_name, last_name, city, country, phone)`: Static method that creates a new customer record in the database. It takes the `id`, `first_name`, `last_name`, `city`, `country`, and `phone` as parameters, creates a new `Customer` object with the provided details, adds it to the session, and commits the transaction to the database.

This model represents customer information and provides a method for creating customer records in the database. It captures details such as the customer's name, city, country, and phone number.
