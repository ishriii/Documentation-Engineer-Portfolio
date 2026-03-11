# Developer Notes

API: Ride Booking API
Base URL: https://api.quickride.com/v1

Auth
Bearer token required.

Header:
Authorization: Bearer ACCESS_TOKEN

Endpoint: POST /rides

Creates a ride request.

Request body

fields:

user_id (int) required

pickup_location (string) required

drop_location (string) required

ride_type (string) optional (mini, sedan, suv)

payment_method (string) required (card, cash, wallet)

Example body

{
  "user_id": 2201,
  "pickup_location": "Andheri East, Mumbai",
  "drop_location": "Bandra Kurla Complex, Mumbai",
  "ride_type": "sedan",
  "payment_method": "card"
}
Response (success)
201
{
  "ride_id": 78021,
  "status": "searching_driver",
  "estimated_arrival": "5 minutes"
}
Errors

400 → bad request
401 → unauthorized
404 → user not found

# Writer's work

# Overview
This API allows users to book ride on QuickRide application.
## Base URL
https://api.quickride.com/v1
## Authentication
Bearer token required
## Header
Authorizaion: Bearer ACCESS_TOKEN
## Endpoint 
POST https://api.quickride.com/v1/rides
## Request Body Parameters
|parameter|Type|Required|Description|
|----|----|----|----|
|user_id|integer|Yes|unique user id|
|pickup_location|string|Yes|pickup location|
|drop_location|string|Yes|drop-off-location|
|ride_type|string|optional|ride type (bike, sedan, SUV)|
|payment_method|string|Yes|payment method (cash, UPI, card) |

## Example body
{

  "user_id": 2201,
  
  "pickup_location": "Andheri East, Mumbai",
  
  "drop_location": "Bandra Kurla Complex, Mumbai",
  
  "ride_type": "sedan",
  
  "payment_method": "card"
  
}

## Response
201

{

  "ride_id": 78021,
  
  "status": "searching_driver",
  
  "estimated_arrival": "5 minutes"
  
  }

  ## Error Codes
  |Code|Status|Description|
  |----|----|----|
  |400|Bad Request|Invalid requst body|
  |401|Unauthorized|Missing or invalid token|
  |404|Not Found|User not found|
