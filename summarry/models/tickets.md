## Tickets Model

The `Tickets` model represents the tickets created by users for help or support. It defines the table structure and provides methods for creating and updating ticket records.

### Model Explanation:

- Table Name: `tickets`
- Columns:
  - `id`: Integer column, primary key.
  - `guid`: String column, stores a unique identifier for the ticket (UUID).
  - `user_id`: Integer column, foreign key referencing the `users` table, specifies the user who created the ticket.
  - `title`: String column, stores the title of the ticket.
  - `description`: String column, stores the description or content of the ticket.
  - `attachment`: String column, stores the filename or path of any attached file.

### Methods:

- `create(user_id, title, description, attachment)`: Static method that creates a new ticket record in the database. It takes the `user_id`, `title`, `description`, and `attachment` as parameters, generates a unique `guid` using UUID, creates a new `Tickets` object with the provided details, adds it to the session, and commits the transaction to the database.
- `update(**details_dict)`: Method that updates the ticket record with the provided details. It takes a dictionary of attribute-value pairs as input, sets the corresponding attributes of the `Tickets` object, and commits the changes to the database.

This model represents the tickets created by users for help or support and provides methods for creating and updating ticket records in the database.
