# Developer's Note


API: Food Delivery API

Base URL

https://api.foodnow.com/v2

Auth
Bearer token required.

Header:

Authorization: Bearer ACCESS_TOKEN

endpoint
GET /orders<br>
Returns list of user orders.

params

user_id int required

limit int optional default 20

offset int optional

status string optional (pending, delivered, cancelled)

example request

GET /orders?user_id=981&limit=10&status=delivered

response 200

{

 "orders":[
 
{

   "order_id": 7782,
   
   "restaurant_name": "Pizza Hub",
   
   "total_amount": 540.50,
   
   "status": "delivered",
   
   "created_at": "2026-03-10T14:20:00Z"
   
  }
  
]

}

errors

401 unauthorized
404 user not found

## Your Task (as Technical Writer)

Turn this into proper API documentation with the following sections:

1️⃣ Overview

2️⃣ Base URL

3️⃣ Authentication

4️⃣ Endpoint

5️⃣ Query Parameters

6️⃣ Example Request

7️⃣ Example Response

8️⃣ Error Codes

# Writer's Work

## Overview

This API allows user to access list of orders.

## Endpoint

Base URL: https://api.foodnow.com/v2

Endpoint path: GET /orders  
Returns list of orders for th specified user.

URL: https://api.foodnow.com/v2/orders

## Authentication
Bearer token required

## Header
Authorization: Bearer ACCESS_TOKEN

## Query Parmeters

|Parameters|Type|Required|Description|
|----|----|----|----|
|user_id|integer|Yes|unique user number|
|limit|integer|optional|limit shows number of orders user can access at a time|
|offset|integer|optional|-|
|status|string|optional|order status (pending, delivered, cancelled)|

## Example Request

GET https://api.foodnow.com/v.2/orders?user_id=981&limit=10&status=delivered

## Response

200

{

 "orders":[
 
  {
  
   "order_id": 7782,
   
   "restaurant_name": "Pizza Hub",
   
   "total_amount": 540.50,
   
   "status": "delivered",
   
   "created_at": "2026-03-10T14:20:00Z"
   
  }
  
 ]
 
}

## Errors

|Error Code|Status|
|----|----|
|401|Unauthorized|
|404|User Not Found|


## Errors in the Documentation

## 1. Overview
   Missing article “a” (This API allows user to access list of orders.)
   Slightly awkward wording
   Correction: 1. This API allows **a** user to retrieve **a** list of their orders.
               2. Retrieves a list of orders for a specific user.

## 2. Typo

Erro: Query Parmters Correction: Query Parameters

## 3. Parameter Table

| Parameter | Type    | Required | Description                                             |
| --------- | ------- | -------- | ------------------------------------------------------- |
| user_id   | integer | Yes      | Unique identifier of the user                           |
| limit     | integer | No       | Maximum number of orders returned. Default is 20        |
| offset    | integer | No       | Number of records to skip for pagination                |
| status    | string  | No       | Filter orders by status (pending, delivered, cancelled) |

## 4. Response
Response (200 OK)
