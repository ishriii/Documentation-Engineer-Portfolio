## Overview
This API allows user to perform payment transaction.

## Endpoint
Base URL: https://api.payment.com

Endpoint path: /api/payments  

Endpoint: POST https://api.payment.com/api/payments

## Header

Content-Type: application/'json'  
Authorization: Bearer <API_KEY>

## Request Body

|Parameter|Type|Required|Description|
|----|----|----|----|
|amount|integer|yes|Payment amount is the smallest currency unit|
|currency|string|yes|Currency code (e.g., INR, USD)|
|payment_method|string|yes|Method used for payment|
|customer_id|string|yes|Unique customer identifier|
|description|string|no|description of the payment| 

## Example request
POST /https://api.payment/.com/api/payments  
Content-Type: application/'json'    
Authorization: Bearer <API_KEY>    
{

  "amount": 50000,
  
  "customer_id": "cust_9283",
  
  "payment_method": "card",
  
  "currency": "INR",
  
  "description": "Order #4582"
  
}

## Example Response
Status code: '201 Created'

{

  "payment_id": "pay_84739",
  
  "amount": 50000,
  
  "currency": "INR",
  
  "status": "successful",
  
  "created_at": "2026-03-12T12:00:00Z"
  
}

## Bad Request

|Error Code|Status|
|----|----|
|400|Bad Request|

{

  "error": "Invalid payment method"
  
}




