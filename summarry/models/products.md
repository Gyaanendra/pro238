## Products Model

The `Products` model represents the products available in the application. It defines the table structure and provides methods for creating and updating product records.

### Model Explanation:

- Table Name: `products`
- Columns:
  - `id`: Integer column, primary key.
  - `guid`: String column, stores a unique identifier for the product (UUID).
  - `name`: String column, stores the name of the product.
  - `image`: String column, stores the image filename or path for the product.
  - `rating`: Integer column, stores the rating of the product.
  - `marked_price`: Float column, stores the marked price of the product.
  - `selling_price`: Float column, stores the selling price of the product.

### Methods:

- `create(name, image, rating, marked_price, selling_price)`: Static method that creates a new product record in the database. It takes the `name`, `image`, `rating`, `marked_price`, and `selling_price` as parameters, generates a unique `guid` using UUID, creates a new `Products` object with the provided details, adds it to the session, and commits the transaction to the database.
- `update(**details_dict)`: Method that updates the product record with the provided details. It takes a dictionary of attribute-value pairs as input, sets the corresponding attributes of the `Products` object, and commits the changes to the database.

This model represents the products available in the application and provides methods for creating and updating product records in the database.
