using System;

namespace Loop_and_functional_programing
{
    class Program
    {
        static void Main(string[] args)
        {
            //DECLARATIONS
            byte chose;
            int N = 0;

            //MAIN
            Console.WriteLine("Select your method");
    
            //METHODS
            Console.WriteLine("1: Natural numbers");
            Console.WriteLine("2: Fibonacci");
            Console.WriteLine("3: Prime numbers");
            chose = Convert.ToByte(Console.ReadLine());
    
            switch (chose) 
            {
                case 1:
                    Console.WriteLine("");
                    Console.WriteLine("Natural numbers");
                    Console.WriteLine("");
                    Console.WriteLine("Write your number");
                    N = Convert.ToInt32(Console.ReadLine());
                    N_Naturals(N);
                    break;
                case 2:
                    Console.WriteLine("");
                    Console.WriteLine("Fibonacci");
                    Console.WriteLine("");
                    Console.WriteLine("How many values do you want?");
                    N = Convert.ToInt32(Console.ReadLine());
                    FIBO(N);
    
                    break;
                case 3:
                    Console.WriteLine("");
                    Console.WriteLine("Prime numbers");
                    Console.WriteLine("");
                    Console.WriteLine("What is your number?");
                    N = Convert.ToInt32(Console.ReadLine());
                    Prime(N);
                    break;
            }
        }
    
        //FORMS
        static int N_Naturals(int N) 
        {
            int result = 0;
    
            if (N > 0) 
            {
                Console.WriteLine("");
                Console.WriteLine("This number is natural {0}", N);
            }
            else 
            {
                Console.WriteLine("");
                Console.WriteLine("This number isn't natural {0}",N);
            }
            
            return result;
        }
        
        static int FIBO(int N) 
        {
            int result = 0, first = 0, second = 1;
            Console.WriteLine("Your results are...");
            Console.WriteLine("1");
            for (int i = 0; i < N; i++)
            {
                result = first + second;
                Console.WriteLine(result);
                second = first;
                first = result;
            }
            
            return result;
        }
        static int Prime(int N) 
        {
            int result = 0, counter = 0;
            for (int i = 1; i < N; i++)
            {
                if (N% i == 0) 
                {
                    counter = counter + 1;
                }
            }
            if (counter == 1) 
            {
                Console.WriteLine("");
                Console.WriteLine("This numbers is prime {0}",N);
            }
            else 
            {
                Console.WriteLine("");
                Console.WriteLine("This number isn't prime",N);
            }
            
            return result;
        }
    }
}