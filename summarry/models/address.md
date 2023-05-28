## Address Model

The `Address` model represents the address information stored in the database. It defines the table structure and provides methods for creating and updating address records.

### Model Explanation:

- Table Name: `address`
- Columns:
  - `id`: Integer column, primary key.
  - `guid`: String column, stores a unique identifier for the address (UUID).
  - `user_id`: Integer column, foreign key referencing the `id` column of the `users` table.
  - `house_number`: String column, stores the house number of the address.
  - `city`: String column, stores the city of the address.
  - `state`: String column, stores the state of the address.
  - `country`: String column, stores the country of the address.
  - `pin_code`: String column, stores the postal code of the address.

### Methods:

- `create(user_id, house_number, city, state, country, pin_code)`: Static method that creates a new address record in the database. It takes the `user_id`, `house_number`, `city`, `state`, `country`, and `pin_code` as parameters, generates a unique `guid` using UUID, creates a new `Address` object with the provided details, adds it to the session, and commits the transaction to the database.
- `update(**details_dict)`: Method that updates the address record with the provided details. It takes a dictionary of attribute-value pairs as input, sets the corresponding attributes of the `Address` object, and commits the changes to the database.

This model represents the address information and provides methods for creating and updating address records in the database.
