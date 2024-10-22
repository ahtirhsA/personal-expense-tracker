# Personal Expense Tracker API

## Description
This project is a Personal Expense Tracker API built with Express.js and SQLite. It allows users to manage their financial transactions, categorizing them as either income or expenses.

## Setup and Run Instructions

### Prerequisites
- Node.js (v14 or higher)
- SQLite3

### Clone the Repository
```bash
git clone https://github.com/ahtirhsA/personal-expense-tracker.git
cd personal-expense-tracker

### Install Dependencies
-npm install

### Run application 
-node index.js  
-It will start the server at (http://localhost:3004)

### Endpoints 

### Create Transaction 

POST /transactions

Request Body: (You can use any valid request body)

{
  "type": "expense",
  "category": 3,
  "amount": 150.75,
  "date": "2024-10-22",
  "description": "Monthly subscription for streaming service"
}  

Responses:

  Invalid input fields:

   Status: 400
   Body: { "error": "Invalid input data. Please check your inputs." }

  Success:

    Status: 201
    Body: { "message": "Transaction successfully created!!" }


### Get All Transactions

GET /transactions

Response:
    Returns an array of transactions.

### Get Transaction by ID

GET /transactions/:id

Responses:

   Success:
     Status: 200 
     Body: Returns the transaction with the specified ID.

   ID does not exist:

     Status: 404 
     Body: { "message": "Transaction does not exist" }

### Update Transaction 

PUT /transactions/:id

Request Body: (You can use any valid request body)

{
    "type": "income",
    "category": 1,
    "amount": 200.00,
    "date": "2024-10-21",
    "description": "Salary for October"
}

Responses:

   ID does not exist:

      Status: 404 Not Found
      Body: { "message": "Transaction does not exist" }
      
    Success:
    
      Status: 200 OK
      Body: { "message": "Transaction updated successfully!!" }


### Delete a Transaction

  DELETE /transactions/:id

  Responses:

   ID does not exist:

     Status: 404 Not Found
     Body: { "message": "Transaction does not exist" }

   Success:

     Status: 200 OK
     Body: { "message": "Transaction deleted successfully!!" }

### Get Summary of Transactions

  GET /summary

  Response:

     Retrieves totalIncome, totalExpense, and Balance.

     

## Postman Screenshots

### Create Transaction
(https://res.cloudinary.com/djzenbn7g/image/upload/v1729611032/yaxrrptlimefh0xzkqia.png)

### Get All Transactions
(https://res.cloudinary.com/djzenbn7g/image/upload/v1729611359/xpzapbtgrtfk4ibfmuow.png)

### Get Transaction by ID
(https://res.cloudinary.com/djzenbn7g/image/upload/v1729611546/g9zmnnt0jkv4jgnbe7ne.png)


### Update Transaction
(https://res.cloudinary.com/djzenbn7g/image/upload/v1729611689/t9scuvgl9y4lhqyxaifl.png)

### Delete Transaction
(https://res.cloudinary.com/djzenbn7g/image/upload/v1729611835/pxbzbp3h8au9v8ot6vk6.png)

### Get Summary
(https://res.cloudinary.com/djzenbn7g/image/upload/v1729611984/api_6_ymlqko.png)

  











