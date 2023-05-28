## Users Model

The `Users` model represents user information and relationships with other models in the application. It defines the table structure and provides methods for creating and updating user records.

### Model Explanation:

- Table Name: `users`
- Columns:
  - `id`: Integer column, primary key.
  - `guid`: String column, stores a unique identifier for the user (UUID).
  - `name`: String column, stores the name of the user.
  - `email`: String column, stores the email address of the user.
  - `password`: String column, stores the password of the user.
  - `contact`: String column, stores the contact information of the user.
- Relationships:
  - `addresses`: One-to-many relationship with the `Address` model. Represents the addresses associated with the user.
  - `orders`: One-to-many relationship with the `Orders` model. Represents the orders placed by the user.
  - `tickets`: One-to-many relationship with the `Tickets` model. Represents the tickets created by the user.

### Methods:

- `create(name, email, password, contact)`: Static method that creates a new user record in the database. It takes the `name`, `email`, `password`, and `contact` as parameters, generates a unique `guid` using UUID, creates a new `Users` object with the provided details, adds it to the session, and commits the transaction to the database.
- `update(**details_dict)`: Method that updates the user record with the provided details. It takes a dictionary of attribute-value pairs as input, sets the corresponding attributes of the `Users` object, and commits the changes to the database.

This model represents user information and provides methods for creating and updating user records in the database. It also defines relationships with other models such as addresses, orders, and tickets.
