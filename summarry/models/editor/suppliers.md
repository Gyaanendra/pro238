## Supplier Model

The `Supplier` model represents a supplier of company products. It defines the table structure and provides a method for creating supplier records.

### Model Explanation:

- Table Name: `suppliers`
- Columns:
  - `id`: Integer column, primary key.
  - `company_name`: String column, stores the name of the supplier's company.
  - `contact_name`: String column, stores the name of the contact person at the supplier's company.
  - `city`: String column, stores the city where the supplier is located.
  - `country`: String column, stores the country where the supplier is located.
  - `phone`: String column, stores the phone number of the supplier.
  - `fax`: String column, stores the fax number of the supplier.

### Methods:

- `create(id, company_name, contact_name, city, country, phone, fax)`: Static method that creates a new supplier record in the database. It takes the `id`, `company_name`, `contact_name`, `city`, `country`, `phone`, and `fax` as parameters, creates a new `Supplier` object with the provided details, adds it to the session, and commits the transaction to the database.

This model represents a supplier of company products and provides a method for creating supplier records in the database. It captures details such as the company name, contact name, location, and contact information of the supplier.
