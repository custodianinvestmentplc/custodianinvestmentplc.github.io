# Get Customers from Insured Database

This method will retreive a paginated collection of [Customers][] from the local database.

## Http Request

-   <code>GET</code> /api/v2/customers/insured-db?pageNumber=1&pageSize=10

### Query Parameters

| Query Parameter | Type    | Description                                |
| --------------- | ------- | ------------------------------------------ |
| page-number     | integer | The Page Number from the List of Customers |
| page-size       | integer | Max Number of records in the page          |

### Request Header

| Name          | Type   | Description                    |
| ------------- | ------ | ------------------------------ |
| Authorization | string | Bearer Token. This is required |

[Customers]: customer-entity.md
