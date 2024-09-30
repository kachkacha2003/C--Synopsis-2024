### # თავი 5 - Implicit და Explicit გადაყვანა C#-ში

## გადაყვანა

C#-ში, გადაყვანა ეხება მონაცემთა ტიპების შორის ურთიერთქმედებას, რაც საშუალებას გვაძლევს გადავიდეთ ერთი ტიპიდან მეორეზე. არსებობს ორი ძირითადი სახის გადაყვანა: Implicit და Explicit.

### 1. **Implicit გადაყვანა**

**Implicit** გადაყვანა ავტომატურად ხდება მაშინ, როდესაც მონაცემთა ტიპი უსაფრთხოა და არ კარგავს მონაცემების ხარისხს. C# ადასტურებს, რომ ეს გადაყვანა უსაფრთხოა და ამიტომ არ საჭიროებს დამატებით კოდს.

**მაგალითი**:

```csharp
int number = 10;
double doubleNumber = number; 
Console.WriteLine("Double Number: " + doubleNumber);
```

ამ მაგალითში, `int` ტიპის `number` ავტომატურად გადადის `double` ტიპში, რაც უსაფრთხოა.

### 2. **Explicit გადაყვანა**

**Explicit** გადაყვანა საჭიროა, როდესაც მონაცემთა ტიპი შეიცვლის ფორმატს და შეიძლება დაკარგოს ინფორმაცია. ამის გამო, საჭიროა კოდის გარკვეული ნაწილი, რათა გამონახოს უსაფრთხო გზები გადაყვანისთვის.

**მაგალითი**:

```csharp
double doubleNumber = 10.5;
int number = (int)doubleNumber; 
Console.WriteLine("Integer Number: " + number);
```

ამ მაგალითში, `double` ტიპის `doubleNumber`Explicit გადაყვანით ხდება `int` ტიპში, მაგრამ ამის გამო ხდება რიცხვის წერტილის დაკარგვა (10.5 ხდება 10).

---

## გადაყვანის ტიპები

### 1. **Implicit Conversion **

C#-ში იმპლიციტური გადაყვანა ხდება ძირითადად შემდეგ ტიპებზე:

- `int` -> `long`
- `float` -> `double`
- `char` -> `int`

**მაგალითი**:

```csharp
char character = 'A';
int asciiValue = character; 
Console.WriteLine("ASCII Value: " + asciiValue);
```

### 2. **Explicit Conversion**

ექსპლიციტური გადაყვანა საჭიროა შემდეგი ტიპების შორის:

- `double` -> `int`
- `long` -> `int`
- `float` -> `int`

**მაგალითი**:

```csharp
float floatNumber = 9.78f;
int intValue = (int)floatNumber; 
Console.WriteLine("Converted Integer Value: " + intValue);
```

---

## მაგალითები

### **Implicit გადაყვანის მაგალითი**:

```csharp
int a = 100;
long b = a; 
Console.WriteLine("Long Value: " + b);
```

### **Explicit გადაყვანის მაგალითი**:

```csharp
double x = 123.456;
int y = (int)x; 
Console.WriteLine("Converted Integer: " + y);
```

---

### **დასკვნა**

- **Implicit** გადაყვანა უსაფრთხოა და ავტომატურად ხდება, რაც ნიშნავს, რომ ინფორმაცია არ იკარგება.
- **Explicit** გადაყვანა საჭიროებს კოდის დამატებას და უნდა ვიყოთ მომზადებული, რომ მონაცემების ნაწილი შეიძლება დაკარგოს.

ამ კონცეფციების ცოდნა მნიშვნელოვანია, რათა სწორად გავაკეთოთ ტიპების გადაყვანა C#-ში და დავაზოგოთ ინფორმაცია.

---

