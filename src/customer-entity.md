### Customer Entity Class

```csharp
public class CustomerEntity
{
    public int Id { get; set; }
    public string UserName { get; set; } = string.Empty;
    public string FirstName { get; set; } = string.Empty;
    public string LastName { get; set; } = string.Empty;
    public string Email { get; set; } = string.Empty;
    public string TelNumber { get; set; } = string.Empty;
    public string Address { get; set; } = string.Empty;
    public string CustomerType { get; set; } = string.Empty;
    public DateTime? DateOfBirth { get; set; }
    public int BrokerId { get; set; }
    public DateTime? CreatedDate { get; set; }
    public bool DeleteStatus { get; set; }
    public string ABSBrokerId { get; set; } = string.Empty;
    public string? TaxId { get; set; }
    public int BrokerAccId { get; set; }
    public string ABSInsuredNum { get; set; } = string.Empty;
}
```
