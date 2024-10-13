## AuthenticatedUserDto

```c#
public class AuthenticatedUserDto
{
    public string? Id { get; set; }
    public string? Email { get; set; }
    public string? BrokerId { get; internal set; }
    public bool IsInternalStaff { get; set; }
    public List<string> Roles { get; set; } = new List<string>();
    public string? BrokerName { get; set; }
}
```

If the currently logged in user is a staff then the following properties will be set:

-   IsInternalStaff - this property will be set to true
-   Email - this property will be set to the email of the staff which is contained in the claim of type "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress"

However, if the currently logged in user is a Broker then the following properties will be set:

-   Id - this property will be set to the Id field in the BrokerAccount table
-   Email - this property will be set to the Broker email
-   BrokerId - this will be set to the ABS BrokerCode. This is set from the claim of type "http://schemas.microsoft.com/ws/2008/06/identity/claims/groupsid"

```c#
protected AuthenticatedUserDto GetAuthenticatedUserDetails()
{
    AuthenticatedUserDto authenticatedUserDetails = new();

    if (User.IsInRole("custodian"))
    {
        authenticatedUserDetails.IsInternalStaff = true;
        authenticatedUserDetails.Email = GetClaimValue(User.Claims, "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress") ?? string.Empty;
    }
    else
    {
        authenticatedUserDetails.Id = GetClaimValue(User.Claims, "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/sid") ?? string.Empty;
        authenticatedUserDetails.Email = GetClaimValue(User.Claims, "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress") ?? string.Empty;
        authenticatedUserDetails.BrokerId = GetClaimValue(User.Claims, "http://schemas.microsoft.com/ws/2008/06/identity/claims/groupsid") ?? string.Empty;
    }

    return authenticatedUserDetails;
}
```
