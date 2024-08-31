# Bash DBMS

## Project Overview
Bash DBMS is a simple database management system implemented using Bash scripting and a terminal interface. It allows users to manage databases and tables directly from the command line.

### Features
- **Main Menu**:
  - **Create Database**: Create a new database.
  - **List Databases**: Display a list of all existing databases.
  - **Drop Database**: Delete a database and all its contents.
  - **Connect Database**: Connect to a specific database to perform table operations.

- **Database Structure**:
  - All databases are saved in the `Databases` directory within the script directory.
  - Each database is stored in a separate directory containing its tables.

### Table Operations
- **Create Table**:
  - Create a new table within the connected database.
  - Supports up to 10 columns, with the first column set as the Primary Key (PK).
  - The PK column cannot be `NULL` and must contain unique values across all rows.
  - For other columns, the user can specify whether each column can accept `NULL` values.
  - The data type (integer or string) must be defined for each column, including the PK.

- **List Tables**:
  - List all tables available in the connected database.

- **Drop Table**:
  - Remove a table from the connected database, deleting all of its data.

- **Insert Into Table**:
  - Add new rows of data to a table.
  - The PK is checked for uniqueness to ensure all records have a unique PK value.
  - Data must conform to the table’s schema, with respect to data types and `NULL` constraints.

- **Update Table**:
  - Update data in a table, including the primary key.
  - If updating the PK, the system checks to ensure the new PK value is unique across the table.
  - Data updates must respect the table’s schema, including `NULL` constraints and data types.

- **Delete From Table**:
  - Delete rows from a table based on a specific column value.
  - Optionally, delete all rows from the table.

- **Select From Table**:
  - Display all rows and columns from a table, including column labels.

## Installation

To install and run the Bash DBMS, follow these steps:

1. **Clone the Repository**:
   - Use Git to clone the repository to your local machine:
     ```bash
     git clone https://github.com/salamaxx97/Data_Base_Using_bash/
     ```

2. **Navigate to the Repository Directory**:
   - Change to the directory where the repository was cloned:
     ```bash
     cd Data_Base_Using_bash

     ```

3. **Ensure All Scripts Are Executable**:
   - Make sure all the Bash scripts in the repository have executable permissions:
     ```bash
     chmod +x *
     ```

4. **Run the Bash DBMS Script**:
   - Execute the main script to start interacting with the DBMS:
     ```bash
     ./Bash_dbms

      ```

## Usage

- From the main menu, manage your databases and connect to them for table operations.
- Databases are stored under the `Databases` directory in the script’s root directory.
- When connected to a database, perform operations on tables within that database.
- Follow the on-screen prompts to interact with the system.

## Additional Notes

- When creating a table, careful consideration is needed for setting up the primary key and column constraints.
- The primary key column cannot accept `NULL` values and must be unique across the table.
- Each column's data type and `NULL` constraints must be defined during table creation.
- The system will enforce uniqueness on the primary key when inserting or updating rows to ensure data integrity, including during PK updates.
