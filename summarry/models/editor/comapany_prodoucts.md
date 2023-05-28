## CompanyProducts Model

The `CompanyProducts` model represents products offered by the company. It defines the table structure and provides a method for creating product records.

### Model Explanation:

- Table Name: `company_products`
- Columns:
  - `id`: Integer column, primary key.
  - `name`: String column, stores the name of the product.
  - `supplier_id`: Integer column, foreign key referencing the `id` column of the `suppliers` table.
  - `unit_price`: Float column, stores the unit price of the product.
  - `package`: String column, stores the package information of the product.
  - `is_discontinued`: Integer column, stores the discontinuation status of the product.

### Methods:

- `create(id, name, supplier_id, unit_price, package, is_discontinued)`: Static method that creates a new product record in the database. It takes the `id`, `name`, `supplier_id`, `unit_price`, `package`, and `is_discontinued` as parameters, creates a new `CompanyProducts` object with the provided details, adds it to the session, and commits the transaction to the database.

This model represents products offered by the company and provides a method for creating product records in the database. It captures details such as the product name, supplier ID, unit price, package information, and discontinuation status.
