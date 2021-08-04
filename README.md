# RAM'in Çalışma prensibi
## Stack 
- RAM'in Stack bölümü değer tipli verileri tutar. Bunlar "int", "long", "float", "double", "decimal", "char", "bool", "byte", "short", "struct", "enum" gibi değişken tipleridir. Buna ek olarak Heap bölümünde tutulan verilerin referans adreslerini barındırır.
```csharp
    class Program
    {
        static void Main(string[] args)
        {
         int number1 = 10;
         int number2 = 20;

         number1=number2; 
         System.Console.WriteLine(number1); //Output : 20

         number2=30;
         System.Console.WriteLine(number2); //Output : 30
         System.Console.WriteLine(number1); //Output : 20
        }
    }
```  

## Heap
- RAM'in Heap bölümü referans tipli verileri tutar. bunlar "string", "object", "class", "interface", "array", "delegate", "pointer" dir. Örneğin integer bir dizi oluşturulurken ( int[] numbers = new int [] {1,2,3,4,5} ) new keywordu ile beraber , Heap'te barınan dataların referans adresi Stack'te tutulur.
```csharp
    class Program
    {
        static void Main(string[] args)
        {
            int [] numbers = new int[] {1,2,3,4,5};

            numbers[4] = 6;

            foreach (var item in numbers)
            {
                System.Console.WriteLine(item); //Output : 1,2,3,4,6
            }
        }
    }
``` 