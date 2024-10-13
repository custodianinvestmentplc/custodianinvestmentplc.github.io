# Retrieve Customer

Retrieve collection of [Customer] either from the Local Db or the Insured Db.

A [Customer] record can exist in one of two databases:

-   The Local Database
-   The Insured Database

Local Database stored customers that have not been authorized by Custodian. Business transactions cannot be created using customers in the Local Db

Insured Database stored customers that have been authorized by Custodian - and these are the customers that can have transactions. Authorized customers have their KYC documentation complete and vetted by Custodian

## Methods

| Method                     | Return Type           | Description                                                     |
| -------------------------- | --------------------- | --------------------------------------------------------------- |
| [Get Customers Local Db]   | [Customer] Collection | Retrieves a paginated list of customers from the local database |
| [Get Customers Insured DB] | [Customer] Collection | Retrieves a paginated list of customers from Insured database   |

[Customer]: /src/customer-entity.md
[Get Customers Local Db]: /src/get-customers-local-db.md
[Get Customers Insured DB]: /src/get-customers-insured-db.md
