### # თავი 7 - მასივები C#-ში

## მასივები

მასივები არის მონაცემების სტრუქტურები, რომლებიც აერთიანებენ ერთ ტიპის რამდენიმე მნიშვნელობის შენახვას. C#-ში მასივები შეიძლება იყოს ერთგანზომილებიანი, მრავალგანზომილებიანი და jagged  მასივები.

### 1. **ერთგანზომილებიანი მასივები**

ერთგანზომილებიანი მასივი არის მონაცემების სტრუქტურა, რომელიც შეიცავს ერთ ტიპის ელემენტებს და ორგანიზებულია ერთი ვერტიკალური ხაზით.

**მაგალითი**:

```csharp
// ერთგანზომილებიანი მასივის შექმნა
int[] numbers = new int[5]; // მასივი, რომელიც შეიცავს 5 ელემენტს

// ელემენტების მინიჭება
numbers[0] = 1;
numbers[1] = 2;
numbers[2] = 3;
numbers[3] = 4;
numbers[4] = 5;

// ელემენტების გაწვდილი
foreach (int number in numbers)
{
    Console.WriteLine(number); // გამოტანს: 1, 2, 3, 4, 5
}
```

### 2. **მრავალგანზომილებიანი მასივები**

მრავალგანზომილებიანი მასივები საშუალებას გაწვდით მრავალ განზომილებაში მონაცემების შენახვას, მაგალითად, ორ ან უფრო მეტი განზომილება.

**მაგალითი**:

```csharp
// 2D (ორი განზომილებიანი) მასივის შექმნა
int[,] matrix = new int[3, 3]; // 3x3 მასივი

// ელემენტების მინიჭება
matrix[0, 0] = 1;
matrix[0, 1] = 2;
matrix[0, 2] = 3;
matrix[1, 0] = 4;
matrix[1, 1] = 5;
matrix[1, 2] = 6;
matrix[2, 0] = 7;
matrix[2, 1] = 8;
matrix[2, 2] = 9;

// ელემენტების გადავლა ფორ ლუპის დახმარებით
for (int i = 0; i < 3; i++)
{
    for (int j = 0; j < 3; j++)
    {
        Console.Write(matrix[i, j] + " "); // გამოტანს: 1 2 3 4 5 6 7 8 9
    }
    Console.WriteLine();
}
```

### 3. **Jagged  მასივები**

Jagged  მასივები არის მასივები, რომლებიც შეიცავს სხვა მასივებს. ეს ნიშნავს, რომ თითოეული ელემენტი არის მასივი და მასივი შეიძლება ჰქონდეს განსხვავებული ზომები.

**მაგალითი**:

```csharp
// Jagged მასივის შექმნა
int[][] jaggedArray = new int[3][]; // 3 ელემენტი, რომლებიც იქნებიან მასივები

// ელემენტების მინიჭება
jaggedArray[0] = new int[2] { 1, 2 }; // 2 ელემენტი
jaggedArray[1] = new int[3] { 3, 4, 5 }; // 3 ელემენტი
jaggedArray[2] = new int[1] { 6 }; // 1 ელემენტი


for (int i = 0; i < jaggedArray.Length; i++)
{
    for (int j = 0; j < jaggedArray[i].Length; j++)
    {
        Console.Write(jaggedArray[i][j] + " "); // გამოტანს: 1 2 3 4 5 6
    }
    Console.WriteLine();
}
```

### 4. **მასივების ინიციალიზაცია**

მასივების ინიციალიზაცია შეიძლება მოხდეს პირდაპირ დეკლარაციის დროს, რაც გვაძლევს შესაძლებლობას სწრაფად ვნიშნოთ ელემენტები.

**მაგალითი**:

```csharp
// ერთგანზომილებიანი მასივის ინიციალიზაცია
int[] fruits = new int[] { 10, 20, 30, 40 }; // ელემენტები ინიცირებული

// 2D მასივის ინიციალიზაცია
int[,] grid = new int[,]
{
    { 1, 2, 3 },
    { 4, 5, 6 },
    { 7, 8, 9 }
};
```

### 5. **მასივების სიგრძე**

მასივების სიგრძე შესაძლებელია მიღება `Length` თვისების გამოყენებით, რაც გვაძლევს მასივის ელემენტების რაოდენობას.

**მაგალითი**:

```csharp
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
Console.WriteLine("მასივის სიგრძე: " + numbers.Length); // გამოტანს: 5

int[,] matrix = new int[3, 3];
Console.WriteLine("მასივის სიგრძე: " + matrix.Length); // გამოტანს: 9 (3x3)
```

---

## მაგალითები

### **ერთგანზომილებიანი მასივის მაგალითი**:

```csharp
int[] evenNumbers = new int[5] { 2, 4, 6, 8, 10 }; // ერთგანზომილებიანი მასივი

foreach (int number in evenNumbers)
{
    Console.WriteLine(number); // გამოტანს: 2, 4, 6, 8, 10
}
```

### **მრავალგანზომილებიანი მასივის მაგალითი**:

```csharp
int[,] twoDimensionalArray = new int[2, 2] { { 1, 2 }, { 3, 4 } }; // 2D მასივი

for (int i = 0; i < 2; i++)
{
    for (int j = 0; j < 2; j++)
    {
        Console.Write(twoDimensionalArray[i, j] + " "); // გამოტანს: 1 2 3 4
    }
    Console.WriteLine();
}
```

### **Jagged (პილწი) მასივის მაგალითი**:

```csharp
int[][] jaggedArray = new int[2][]; // Jagged მასივი

jaggedArray[0] = new int[] { 1, 2 };
jaggedArray[1] = new int[] { 3, 4, 5 }; // შეიძლება განსხვავებული სიგრძე

foreach (var arr in jaggedArray)
{
    foreach (var item in arr)
    {
        Console.Write(item + " "); // გამოტანს: 1 2 3 4 5
    }
    Console.WriteLine();
}
```

---

### **დასკვნა**

- **მასივები** საშუალებას აძლევს ერთ ტიპის მრავალ მონაცემს ერთ ადგილზე შეინახოს.
- **მრავალგანზომილებიანი** მასივები გამოყენება საშუალებას იძლევა მონაცემების ორგანიზებულად შენახვისა და წვდომის.
- **Jagged  მასივები** საშუალებას იძლევა სხვადასხვა სიგრძის მასივების გამოყენება.
- **მასივების სიგრძე** მარტივად მიიღება `Length` თვისების გამოყენებით.

მასივების გამოყენება C#-ში საჭიროა მონაცემების ეფექტური მართვისთვის და ცალკეულ ელემენტებზე მუშაობის გამარტივებისთვის.

