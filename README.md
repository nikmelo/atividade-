Aqui vai um exemplo de implementação do algoritmo Bubble Sort em C# para ordenar os algarismos:

```
using System;

class Program
{
    static void Main()
    {
        int[] numeros = { 1, 5, 8, 9, 7, 3, 2, 4, 6 };
        Console.WriteLine("Array antes da ordenação:");
        ImprimirArray(numeros);

        BubbleSort(numeros);

        Console.WriteLine("Array após a ordenação:");
        ImprimirArray(numeros);
    }

    static void BubbleSort(int[] array)
    {
        int n = array.Length;
        for (int i = 0; i < n - 1; i++)
        {
            for (int j = 0; j < n - i - 1; j++)
            {
                if (array[j] > array[j + 1])
                {
                    // Troca os elementos
                    int temp = array[j];
                    array[j] = array[j + 1];
                    array[j + 1] = temp;
                }
            }
        }
    }

    static void ImprimirArray(int[] array)
    {
        foreach (var item in array)
        {
            Console.Write(item + " ");
        }
        Console.WriteLine();
    }
}
```

Este código define um array de inteiros, imprime o array antes da ordenação, ordena o array usando o algoritmo Bubble Sort e, por fim, imprime o array ordenado. O Bubble Sort funciona comparando cada par de elementos adjacentes e trocando-os se estiverem na ordem errada. Esse processo é repetido até que o array esteja ordenado.

A saída será:

```
Array antes da ordenação:
1 5 8 9 7 3 2 4 6 
Array após a ordenação:
1 2 3 4 5 6 7 8 9 
```
