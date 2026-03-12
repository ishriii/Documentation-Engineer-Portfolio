# Developer's Data

## Endpoint
POST /api/payments

## Description

Creates a new payment transaction.

## Request Body

Field	Type	Required	Description

amount	integer	yes	Payment amount in smallest currency unit

currency	string	yes	Currency code (e.g., INR, USD)

payment_method	string	yes	Method used for payment

customer_id	string	yes	Unique customer identifier

description	string	no	Payment description

Example Request

{

  "amount": 50000,
  
  "currency": "INR",
  
  "payment_method": "card",
  
  "customer_id": "cust_9283",
  
  "description": "Order #4582"
  
}

Example Success Response

Status Code: 201 Created

{

  "payment_id": "pay_84739",
  
  "amount": 50000,
  
  "currency": "INR",
  
  "status": "successful",
  
  "created_at": "2026-03-12T12:00:00Z"
  
}

Example Error Response

Status Code: 400 Bad Request

{

  "error": "Invalid payment method"
  
}

Your Task

Write complete API documentation including:

1️⃣ Endpoint
2️⃣ Method
3️⃣ Description
4️⃣ Request Body Table
5️⃣ Example Request
6️⃣ Success Response
7️⃣ Error Responses
8️⃣ Status Codes







