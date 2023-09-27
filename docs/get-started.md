# Getting Started with Freddy Candy Store APIs

Welcome to the Freddy Candy Store API documentation. This guide will help you quickly get started and explain how to use our APIs.

## Prerequisites

Before you start using our APIs, please ensure you have the following:

- Access Credentials: You should have the username and password of your account to use the APIs. If you haven't received them, please contact our support team at support@freddystore.com.

## Using Our APIs

The APIs provide various endpoints to manage and maintain the Freddy Candy Store platform. Here are the essential endpoints you can use:

1. Login

```shell
POST /login
```
Purpose: Log into your account.
Response: A successful login will return an `access_token` and a `refresh_token`. The `access_token` is valid for 15 minutes, and the `refresh_token` is valid for 30 days.

[Click here to view the full API reference](/api-reference#/default/post_login)


2. Refresh Access Token

```shell
POST /refresh
``` 
Purpose: Generate a new access token using a valid refresh token.
Authorization: Bearer refresh_token
Response: A successful request will return a new `access_token`.

[Click here to view the full API reference](/api-reference#/default/post_refresh)


3. Get Dashboard Information

```shell
GET /dashboard
``` 
Purpose: Retrieve data for your dashboard, including revenue information, bestsellers, etc.
Authorization: Bearer access_token
Response: The response will include data for today, the last 7 days, and the last 12 months, as well as information about best-selling products.

[Click here to view the full API reference](api-reference#/default/get_dashboard)

4. Index Orders

```shell
GET /orders
``` 
Purpose: Retrieve a list of your orders.
Query parameters for filtering orders by page, product name, status, date, and price.
Authorization: Bearer access_token

[Click here to view the full API reference](/api-reference#/default/get_orders)

## Authentication

All API endpoints that require authentication (e.g., access tokens) should include an Authorization header in the request with the format Bearer YourAccessToken.

Please note that access tokens are only valid for 15 minutes, so make sure to handle token expiration by using refresh tokens when necessary.

For more detailed information and examples, refer to our API Reference.

If you have any questions or encounter issues while using our APIs, don't hesitate to reach out to our support team at support@freddystore.com.
