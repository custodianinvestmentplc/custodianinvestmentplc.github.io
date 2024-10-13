Below is a sample JWT token returned by the Broker API when a Broker logs in

```
{
    "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress": "adedoyinolorunfemi2020@gmail.com",
    "brokerId": "B1017/HO",
    "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/sid": "1135",
    "http://schemas.microsoft.com/ws/2008/06/identity/claims/groupsid": "B1017/HO",
    "identityNo": "1135",
    "email": "adedoyinolorunfemi2020@gmail.com",
    "role": ["MOTOR(THIRD PARTY)", "MOTOR(COMPREHENSIVE)", "MOTOR(THIRD PARTY,FIRE,THEFT)"],
    "http://schemas.microsoft.com/ws/2008/06/identity/claims/role": ["MOTOR(THIRD PARTY)", "MOTOR(COMPREHENSIVE)", "MOTOR(THIRD PARTY,FIRE,THEFT)"],
    "nbf": 1728733137,
    "exp": 1728736737,
    "iss": "nil",
    "aud": "nil"
}
```

The token can either be created for a staff or a broker. A staff will have the role 'Custodian'
