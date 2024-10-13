# Get Customers from Local Database

This method will retreive a paginated collection of [Customer] from the local database.

## Http Request

-   <code>GET</code> /api/v2/customers/local-db?page-number=1&page-size=10

### Query Parameters

| Query Parameter | Type    | Description                                |
| --------------- | ------- | ------------------------------------------ |
| page-number     | integer | The Page Number from the List of Customers |
| page-size       | integer | Max Number of records in the page          |

### Request Header

| Name          | Type   | Description                    |
| ------------- | ------ | ------------------------------ |
| Authorization | string | Bearer Token. This is required |

[Customer]: /src/customer-entity.md
