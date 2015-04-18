using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int a = Convert.ToInt32(Console.ReadLine());
            int b = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine(RBB(a, b));
            Console.ReadLine();
        }

        static bool RBB(int a, int b)
        {
            int summa_a = 1;
            int summa_b = 1;
            for (int i = 2; i < a; i++)
            {
                if (a % i == 0) summa_a += i;
            }
            for (int p = 2; p < b; p++)
            {
                if (b % p == 0) summa_b += p;
            }
            return (summa_a == b && summa_b == a);
        }
     }
}
