# Задача!!!
>Написать программу, которая из имеющегося массива строк формирует массив из строк,
длина которых меньше либо равна 3 символам. Первоначальный массив можно ввести с
клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомндуется
пользоваться коллекциями, лучше обойтись исключительно массивами.
---
# Решение задачи:
> задаем массив `string[] array`
```C#

string[] array = new string[] {"Hello", "2", "world", ":-)"};

```
- Создание метода `string[] SortedArray`
   >создаем метод сортирующий символы из массива.
сначала отсчитываем количество, удовлетворяющих требований, для определения длинны нового массива.
создаем массив по выясненому количествуи заносим туда символы удовлетворяющие требованиям.
```C#
string[] SortedArray (string[] array)
{
    int count = 0;
    for (int i = 0; i < array.Length; i++)
    {
        string simvol = array[i];
        if (simvol.Length <= 3)
        {
            count++;
        }
    }
    string[] arraySimvol = new string[count];
    for (int i = 0, j = 0; i < array.Length; i++)
    {
        string simvol = array[i];
        if (simvol.Length <= 3)
        {
            arraySimvol[j] = simvol;
            j++;
        }
    }
    return arraySimvol;
}
```
- Создание метода ` PrintArray`
   >создаем метод для вывода информации из массивов с использованием цеклического вывода каждого элемента массива.
```C#

void PrintArray (string[] array)
{
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write($"{array[i]}  ");
    }
    Console.WriteLine();
}
```

## Создаем `" код"` для вызова методов и обработки информации через консоль.
  >выводим поясняющую информационную строку для пользователя в консоле: " Символы - "
  >- присваиваем введенное в консоле от пользователя символы `string inStringSimvol = console.ReadLine()`
  >- присваиваем массиву преобразованную строку через метод `string[] array = SortedArray`
  >Console.WriteLine();
Console.Write("Cимволы - ");
PrintArray(array);
Console.WriteLine();
Console.Write("Введенные символы длинной меньше либо равны 3 -    ");
PrintArray(SortedArray(array));
Console.WriteLine();
```C#

Console.WriteLine();
Console.Write("Cимволы - ");
PrintArray(array);
Console.WriteLine();
Console.Write("Введенные символы длинной меньше либо равны 3 -    ");
PrintArray(SortedArray(array));
Console.WriteLine();
```

# **END**

---

