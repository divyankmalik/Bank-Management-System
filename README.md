# Bank Management System

## Description
The **Bank Management System** is a C++ console-based project designed to simulate the functionalities of a bank. It allows users to manage customer accounts, perform transactions, and maintain a record of all customers. This project demonstrates object-oriented programming principles such as encapsulation, data abstraction, and structuring with classes. It is an ideal project for beginners to learn and practice C++ programming concepts.

---

## Features
1. **Create New Account:** Users can create a new customer account by entering details such as name, ID, address, contact number, and initial cash balance.
2. **View Customer List:** Displays the list of all customers, including their name, ID, address, contact number, and cash balance.
3. **Update Account Information:** Allows users to modify an existing customer's details, such as name, address, and cash balance.
4. **Search for Account Details:** Users can search for a customer account using the customer's unique ID and view their details.
5. **Perform Transactions:** Supports:
   - Deposits: Add cash to a customer's account.
   - Withdrawals: Deduct cash from a customer's account (with validation to prevent overdrafts).
6. **Delete Accounts:**
   - Delete a specific customer's account using their unique ID.
   - Delete all customer records at once.
7. **Exit Program:** Safely exit the application.

---

## Project Structure
### Class: `Bank`
This is the main class that encapsulates the functionality of the system.

#### Private Attributes:
- **`total`**: Keeps track of the total number of customers.
- **`id`**: Temporarily stores the ID of a customer for searching, updating, or deleting records.
- **`struct person`**: Stores customer details, including:
  - `name`: Customer's name.
  - `ID`: Unique identifier for the customer.
  - `address`: Customer's address.
  - `contact`: Customer's contact number.
  - `cash`: Customer's current account balance.

#### Public Methods:
1. **`choice()`**: Displays the menu and handles user input for selecting options.
2. **`perData()`**: Collects data for a new customer account.
3. **`show()`**: Displays all customer records.
4. **`update()`**: Updates the details of an existing customer account.
5. **`search()`**: Searches for and displays details of a specific account.
6. **`transactions()`**: Handles deposits and withdrawals for a specific customer.
7. **`del()`**: Deletes a specific account or all accounts.

---

## How It Works
### 1. Menu Options
The program presents the user with a menu of operations, including account creation, transaction handling, and account deletion.

### 2. Handling Customer Data
Each customer is represented as an instance of the `person` structure, and all customer details are stored in an array.

### 3. User Input
The program uses the `getch()` function to accept user input for menu selection. Based on the input, the corresponding method is invoked.

### 4. Transactions
The `transactions()` function allows users to deposit or withdraw cash. For withdrawals, it validates whether the customer has sufficient funds.

### 5. Deletion
- **Specific Record Deletion:** Shifts the records after the deleted record to maintain the array.
- **Full Deletion:** Resets the `total` counter, effectively clearing all records.

---

## Example Usage
### Input:
```
1. Create New Account
   Enter name: John
   Enter ID: 123
   Enter address: 456 Elm St
   Enter contact: 9876543210
   Enter cash: 5000
```

### Output:
```
Account created successfully!
```

### Input:
```
5. Perform Transaction
   Enter ID: 123
   Existing Cash: 5000
   Press 1 to deposit
   Amount to deposit: 2000
```

### Output:
```
Transaction successful!
New Cash: 7000
```

---

## Technologies Used
- **Language:** C++
- **Libraries:**
  - `<iostream>`: For input and output.
  - `<conio.h>`: For `getch()` to handle menu input.
  - `<windows.h>`: For adding delays and clearing the screen.

---

## Prerequisites
- C++ Compiler (e.g., GCC, MSVC)
- Basic knowledge of C++ programming concepts.

---

## How to Run
1. Clone the repository or download the code.
2. Compile the code using a C++ compiler:
   ```
   g++ BankManagementSystem.cpp -o BankManagementSystem
   ```
3. Run the executable:
   ```
   ./BankManagementSystem
   ```
4. Follow the on-screen instructions.

---

## Future Enhancements
- Add file handling to save and load customer data between sessions.
- Improve input validation to handle incorrect or invalid data.
- Introduce a graphical user interface (GUI) for better usability.

---
