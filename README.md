# Advance_web_practical


Practical 1
```c#
using System;
namespace TYIT
{
    public class prog1
    {
        public static void fibo()
        {
            int n1 = 0, n2 = 1, n3, i, number;
            Console.Write("Enter the number of elements: ");
            number = Convert.ToInt32(Console.ReadLine());
            Console.Write(n1 + " " + n2 + " ");   
            for (i = 2; i < number; ++i)   
            {
                n3 = n1 + n2;
                Console.Write(n3 + " ");
                n1 = n2;
                n2 = n3;
            }
            Console.WriteLine();
        }

        public static void isVowel()
        {
            Console.WriteLine("Enter character");
            char ch = Convert.ToChar(Console.ReadLine().ToLower());
            if('a' == ch || 'e' == ch || 'i' == ch || 'o' == ch || 'u' == ch)
            {
                Console.WriteLine(ch + " is Vowel");
            }
            else
            {
                Console.WriteLine(ch + " is not Vowel");
            }
       

        }

        public static void reversNum() {
            Console.WriteLine("Enter number");
            int num = Convert.ToInt32(Console.ReadLine());
            int digit = 0;
            int rev = 0;
            int sum = 0;
            while (num > 0)
            {
                digit = num % 10;
                rev = rev * 10 + digit; 
                sum += digit;
                num = num / 10;

            }
            Console.WriteLine("reverse " + rev);
            Console.WriteLine("Sum " + sum);
        }
        public static void Main(String[] args)
        {
            fibo();
            isVowel();
            reversNum();
        }
    }
}

```
