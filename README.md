# Advance_web_practical

<h2>Practical 1</h2>

Practical 1.c
Aim: Create an application that receives the (Student Id, Student Name, Course Name, Date of
Birth) information from a set of students. The application should also display the
information of all the students once the data entered.
```c#
using System;

namespace practical_1c
{
    internal class Program
    {
        /// id name course dob
        int id, dob;
        string name, course;

        public int Id
        {
            set { id = value; }
            get { return id; }  
        }

        public int Dob
        {
            set { dob = value; }
            get { return dob; }
        }

        public string Name
        {
            get;set;
        }

        public string Course
        {
            get;set;
        }

        public Program(int id, string name, string course, int dob) {
            Id = id; 
            Name = name; 
            Course = course; 
            Dob = dob;
            
        }

        public void display()
        {
            Console.WriteLine("id :" + Id + ", name :" + Name + ", course :" + Course + ", dob :" + Dob);
        }

        
        static void Main(string[] args)
        {
            Program a = new Program(1, "Omkar", "BSC-IT", 2004);
            a.display();

            Console.ReadLine();
        }
    }
}

```

Practical 1.d
Aim:  Create an application to demonstrate following operations <br>
i. Generate Fibonacci series. <br>
ii. Test for prime numbers.<br>
iii. Test for vowels. <br>
iv. Use of foreach loop with arrays<br>
v. Reverse a number and find sum of digits of a number.

<i>(Incomplete code)</i>
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
