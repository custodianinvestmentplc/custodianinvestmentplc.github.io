## <code>POST</code> api/customer/create

Request Payload

The following fields are mandatory:

-   firstName
-   userName
-   address
-   customerType (enum - either Individual or Corporate)

Other key points

-   The taxId field cannot be more than 13 characters

### Business Logic

-   Only a Brker can create a customer
