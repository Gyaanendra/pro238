## Flask API

The provided code defines a Flask API using the Blueprint feature. It imports necessary modules and models for database operations and file handling.

### Code Explanation:

1. Import necessary modules and packages.
2. Create a Flask blueprint named `api` with the URL prefix of `'/api'`.
3. Define API routes for different operations:
   - `/login`: Handles the login functionality. Retrieves email and password from the request JSON, queries the database to find a matching user, and stores user information in the session if found.
   - `/logout`: Handles the logout functionality. Clears the email and user ID stored in the session.
   - `/add-address`: Creates a new address for the user. Retrieves address details from the request JSON and inserts them into the database.
   - `/create-order`: Creates a new order. Retrieves product ID, address ID, and amount from the request JSON and inserts the order details into the database.
   - `/submit-help`: Submits a help request. Retrieves title, description, and attachment file from the request form data, saves the attachment file to a specific folder, and inserts the help request details into the database.
   - `/download/<path:filename>`: Allows downloading of the specified file from the attachment folder.
   - `/search-order`: Searches for a specific order. Retrieves the order ID from the request query parameters, queries the database for the order details, and returns the order information.
   - `/execute`: Executes a database query provided in the request JSON. Executes the query using the database engine and returns the query result as JSON.
   - `/get-customer`: Retrieves customer information based on the provided customer ID query parameter.
4. Each route handler returns JSON responses with appropriate status codes and messages.
5. The code demonstrates how to define API routes, handle JSON and form data, perform database operations, and handle file uploads and downloads.

This code provides an API interface for login, logout, address management, order creation, help request submission, database query execution, and customer retrieval functionalities.
