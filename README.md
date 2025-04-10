# Publico
using System;

class Program
{
    static void Main()
    {
        Random rnd = new Random();
        int numeroSecreto = rnd.Next(1, 101);
        int intentos = 0;

        Console.WriteLine("¡Adivina el número (1-100)!");

        while (true)
        {
            Console.Write("Tu intento: ");
            int intento = Convert.ToInt32(Console.ReadLine());
            intentos++;

            if (intento == numeroSecreto)
            {
                Console.WriteLine($"¡Correcto! Lo lograste en {intentos} intentos.");
                break;
            }
            Console.WriteLine(intento < numeroSecreto ? "Más alto" : "Más bajo");
        }
    }
}