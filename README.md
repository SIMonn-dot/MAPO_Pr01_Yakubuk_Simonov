using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace VS_Пр_01_Якубук_Симонов
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Введите число от 1 до 10");
            string a = Console.ReadLine();

            int A = Convert.ToInt32(a);
           
            GenerateTableUmnaz(A);


            void GenerateTableUmnaz(int size)
            {
               
                
                //Вывод заголовка
                for (int i = 1; i <= size; i++)
                {
                    Console.Write($"{i,3} ");
                }
                Console.WriteLine();
                Console.WriteLine(new string('-', size * 4 + 3));

                //Вывод таблицы
                for (int i = 1; i <= size; i++)
                {
                    Console.Write($"{i,2} |");
                    for (int j = 1; j <= size; j++)
                    {
                        Console.Write($"{i * j,3} ");
                    }
                    Console.WriteLine();
                }
            }
            Console.ReadKey();
        }
    }
}
