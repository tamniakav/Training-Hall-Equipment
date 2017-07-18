# Training-Hall-Equipment
Just another repository
using System;

namespace Training_Hall_Equipment_2
{
    class Program
    {
        static void Main(string[] args)
        {
            double budget = double.Parse(Console.ReadLine());
            int countOfItems = int.Parse(Console.ReadLine());

            double totalSum = 0;

            for (int i = 0; i < countOfItems; i++)
            {
                string nameOfItem = Console.ReadLine();
                double price = double.Parse(Console.ReadLine());
                int count = int.Parse(Console.ReadLine());

                double sum = price * count;
                totalSum += sum;

                if (count == 1)
                {
                    Console.WriteLine($"Adding 1 {nameOfItem} to cart.");
                }
                else
                {
                    Console.WriteLine($"Adding {count} {nameOfItem}s to cart.");
                }
            }

            Console.WriteLine($"Subtotal: ${totalSum:f2}");

            double moneyLeft = Math.Abs(budget - totalSum);

            if (budget >= totalSum)
            {
                Console.WriteLine($"Money left: ${moneyLeft:f2}");
            }
            else
            {
                Console.WriteLine($"Not enough. We need ${moneyLeft:f2} more.");
            }
        }
    }
}
