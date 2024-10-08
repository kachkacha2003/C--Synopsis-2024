### # თავი 8 - შესავალი ობიექტზე ორიენტირებული პროგრამირების I

## ობიექტზე ორიენტირებული პროგრამირება (OOP)

ობიექტზე ორიენტირებული პროგრამირება არის პროგრამირების პარადიგმა, რომელიც გამოიყენებს ობიექტების შექმნას, რაც საშუალებას გვაძლევს შევქმნათ უფრო მოდულური და კოდირებული პროგრამები. OOP-ის ძირითადი კონცეფციები არიან: **კლასები**, **ობიექტები**, **ინკაპსულაცია**, **აბსტრაქცია**, **პოლიმორფიზმი**

### 1. **კლასები**

კლასი არის თეორიული მონახაზი, რომელიც აღწერს ობიექტების საერთო თვისებებსა და ქცევას. კლასში ვიწერთ მისაწვდილი ტიპების (Fields) და მეთოდების (Methods) აღწერილობას.

**მაგალითი**:

```csharp
// კლასის შექმნა
public class Car
{
    // თვისებები (Fields)
    public string Make;
    public string Model;
    public int Year;

    // კონსტრუქტორი
    public Car(string make, string model, int year)
    {
        Make = make;
        Model = model;
        Year = year;
    }

    // მეთოდი
    public void DisplayInfo()
    {
        Console.WriteLine($"Auto: {Make} {Model}, {Year}"); // ავტომობილის ინფორმაცია
    }
}
```

### 2. **ობიექტები**

ობიექტი არის კლასის კონკრეტული ინსტანსი. როდესაც კლასის სქემას ვქმნით, ობიექტი წარმოადგენს კონკრეტულ მაგალითს ამ კლასისგან.

**მაგალითი**:

```csharp
// ობიექტის შექმნა
Car myCar = new Car("Toyota", "Corolla", 2021); // Car კლასის ახალი ობიექტი

// ობიექტის მეთოდის გამოყენება
myCar.DisplayInfo(); // გამოიტანს: Auto: Toyota Corolla, 2021
```

### 3. **ინკაპსულაცია**

ინკაპსულაცია არის პროცესი, რომლის დროსაც კლასის შიდა მონაცემები და მეთოდები დაცულია და მხოლოდ კლასის მეშვეობითაა შესაძლებელი მათზე წვდომა. ეს ეხმარება მონაცემების დაცვას და უსაფრთხოების გაზრდას.

**მაგალითი**:

```csharp
public class BankAccount
{
    // კერძო (private) თვისება
    private decimal balance;

    // კონსტრუქტორი
    public BankAccount(decimal initialBalance)
    {
        balance = initialBalance;
    }

    // საჯარო მეთოდი, რომ თანხის დამატება
    public void Deposit(decimal amount)
    {
        if (amount > 0)
        {
            balance += amount;
            Console.WriteLine($"გადახდა: {amount} ლარი. ახალი ბალანსი: {balance}");
        }
    }

    // public მეთოდი, რომ ბალანსი გამოიძახოს
    public decimal GetBalance()
    {
        return balance; // ბალანსის დაბრუნება
    }
}
```


### **დასკვნა**

- **OOP** ხელს უწყობს პროგრამების ორგანიზებას და მოდულურობას.
- **კლასები** აღწერენ ობიექტების ქცევას და თვისებებს.
- **ობიექტები** კლასების კონკრეტული მაგალითებია.


ეს საფუძვლები დაგეხმარებათ ობიექტზე ორიენტირებული პროგრამირების უკეთ გაგებაში და C#-ში უფრო კომპლექსური პროგრამების შექმნაში.

