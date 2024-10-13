## <code>POST</code> api/customer/create

Request Payload

```
{
    "firstName": "string",
    "userName": "string",
    "lastName": "string",
    "email": "string",
    "phoneNumber": "string",
    "address": "string",
    "customerType": "Individual",
    "dateOfBirth": "2024-10-12T12:00:33.345Z",
    "taxId": "string"
}
```

The following fields are mandatory:

-   firstName
-   userName
-   address
-   customerType (enum - either Individual or Corporate)

Other key points

-   The taxId field cannot be more than 13 characters

### Business Logic

-   Only a Brker can create a customer
