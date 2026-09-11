# Interacting With Relational DB

A Jupyter Notebook project demonstrating how to connect to and query a MySQL relational database using Python.

## Overview

This project uses the `sakila` sample database (a standard MySQL demo database of a DVD rental store) to practice writing and executing SQL queries from a Python/Jupyter environment.

## Project Structure

```
.
├── src/
│   └── Interactingwithsqldb.ipynb   # Main notebook: DB connection & queries
├── .env                              # Local environment variables (not tracked)
├── .gitignore
└── README.md
```

## Prerequisites

- Python 3.x
- MySQL Server running locally
- Jupyter Notebook / VS Code with Jupyter extension
- The `sakila` sample database imported into your local MySQL instance

## Setup

1. **Clone the repository**
   ```
   git clone https://github.com/BLINUXM/Intracting_With_RelationalDB.git
   cd Intracting_With_RelationalDB
   ```

2. **Install dependencies**
   ```
   pip install python-dotenv ipython-sql mysql-connector-python
   ```

3. **Configure environment variables**

   Create a `.env` file in the project root (this file is git-ignored and should never be committed):
   ```
   DB_HOST=localhost
   DB_PORT=3306
   DB_USER=your_username
   DB_PASSWORD=your_password
   DB_NAME=sakila
   ```

4. **Load the SQL magic extension**

   In the first cell of the notebook:
   ```
   %load_ext sql
   ```

   Then connect using the SQL magic syntax, e.g.:
   ```
   %sql mysql+mysqlconnector://DB_USER:DB_PASSWORD@DB_HOST:DB_PORT/DB_NAME
   ```

5. **Run the notebook**

   Open `src/Interactingwithsqldb.ipynb` in VS Code or Jupyter and run the cells in order.

## Security Note

This project loads database credentials from a `.env` file, which is excluded from version control via `.gitignore`. Never commit real credentials to the repository.

## License

This project is for educational purposes.