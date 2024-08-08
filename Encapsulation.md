
### Definition

Encapsulation is the mechanism of restricting access to some of an object's components and protecting the object's internal state from unauthorized modification. It bundles the data (variables) and methods (functions) that operate on the data into a single unit called a class.

### Benefits

- **Data Hiding**: Prevents unauthorized access to the data.
- **Modularity**: Increases modularity by keeping different parts of a system isolated.
- **Maintenance**: Easier to maintain and modify existing code.

### Example

```csharp
public class BankAccount
{
    private decimal balance; // Private field

    // Public method to get the balance
    public decimal GetBalance()
    {
        return balance;
    }

    // Public method to deposit money
    public void Deposit(decimal amount)
    {
        if (amount > 0)
        {
            balance += amount;
        }
    }

    // Public method to withdraw money
    public void Withdraw(decimal amount)
    {
        if (amount > 0 && amount <= balance)
        {
            balance -= amount;
        }
    }
}
```

#### Usage

```csharp
public class Program
{
    public static void Main(string[] args)
    {
        BankAccount account = new BankAccount();
        account.Deposit(1000);
        account.Withdraw(500);
        Console.WriteLine("Balance: " + account.GetBalance());
    }
}
```
#OOP 