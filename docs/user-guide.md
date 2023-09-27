# Getting Started with Freddy Candy Store APIs

Welcome to the Freddy Candy Store API documentation. This guide will help you quickly get started and explain how to use our APIs.

## Prerequisites

Before you start using our APIs, please ensure you have the following:

- Access Credentials: You should have the username and password of your account to use the APIs. If you haven't received them, please contact our support team at support@freddystore.com.

## Using Our APIs

The APIs provide various endpoints to manage and maintain the Freddy Candy Store platform. Here are the essential endpoints you can use:

1. Login
Endpoint: /login (HTTP POST)
Purpose: Log into your account.
Parameters:
username: Your account username.
password: Your account password.
Response: A successful login will return an access_token and a refresh_token. The access_token is valid for 15 minutes, and the refresh_token is valid for 30 days.
Example request body:

```json
{
  "username": "YourUsername",
  "password": "YourPassword"
}
```

2. Refresh Access Token
Endpoint: /refresh (HTTP POST)
Purpose: Generate a new access token using a valid refresh token.
Parameters:
refresh_token: Bearer refresh token for authentication.
Response: A successful request will return a new access_token.
Example request header:

json
Copy code
Authorization: Bearer YourRefreshToken

3. Get Dashboard Information
Endpoint: /dashboard (HTTP GET)
Purpose: Retrieve data for your dashboard, including revenue information and bestsellers.
Parameters:
access_token: Bearer access token for authentication.
Response: The response will include data for today, the last 7 days, and the last 12 months, as well as information about best-selling products.
Example request header:

json
Copy code
Authorization: Bearer YourAccessToken

4. Index Orders
Endpoint: /orders (HTTP GET)
Purpose: Retrieve a list of your orders.
Parameters:
access_token: Bearer access token for authentication.
Query parameters for filtering orders by page, product name, status, date, and price.
Example request header:

json
Copy code
Authorization: Bearer YourAccessToken
Example request URL with query parameters:

css
Copy code
/orders?page[number]=1&filter[product_name]=YourProduct&filter[status]=Shipped

## Authentication

All API endpoints that require authentication (e.g., access tokens) should include an Authorization header in the request with the format Bearer YourAccessToken.

Please note that access tokens are short-lived, so make sure to handle token expiration by using refresh tokens when necessary.

For more detailed information and examples, refer to our API Reference.

If you have any questions or encounter issues while using our APIs, don't hesitate to reach out to our support team at support@freddystore.com.

Happy API exploring!
