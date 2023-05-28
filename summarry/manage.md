## Flask Database Seeder

The provided code is a Flask CLI command for seeding the database with initial data. It imports necessary modules, defines data in JSON format, and includes functions to recreate the database tables and populate them with seed data.

### Code Explanation:

1. Import necessary modules and packages.
2. Define JSON data for users and products.
3. Define functions for recreating the database and populating it with seed data:
   - `recreate_db`: Drops all tables, creates new tables, and commits the changes.
   - `seeder`: Iterates through the JSON data and creates database records for users and products using their respective model classes.
   - Additionally, it reads data from CSV files and creates records for editor-related models (`Customer`, `Supplier`, `CompanyProducts`, `CompanyOrders`, `OrderItems`).
4. Define a Flask CLI command using `@cli.command()` decorator to run the database seeding process.
5. The command `rsd` (short for "recreate and seed database") calls the `recreate_db` and `seeder` functions to recreate the database and populate it with seed data.
6. If the script is directly executed (not imported), it runs the Flask CLI using `cli()`.

This code provides a convenient way to recreate and seed the database with initial data using a Flask CLI command. It demonstrates the use of CLI commands, importing data from JSON and CSV files, and interacting with the database models.
