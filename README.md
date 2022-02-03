 ****List Of .NET programmes****<br>
**1.Binary triangle**<br>
 using System;<br>

namespace Exercises<br>
{
    class BinaryTriangle<br>
    {<br>
        static void Main(string[] args)<br>
        {<br>
            int number, digit = 1;<br>
            Console.Write("\n Enter the number of lines:");<br>
            number = Convert.ToInt32(Console.ReadLine());<br>
            for (int i = 1; i <= number; i++)<br>
            {<br>
                f<br>or (int space = number - i;space > 0;space--) 
                {<br>
                    Console.Write(" ");<br>

                }<br>
                for (int j = 0; j < i; j++)<br>
                {<br>
                    Console.Write(digit + " ");<br>
                    digit = (digit == 1) ? 0 : 1;<br>

                }<br>
                Console.Write("\n");<br>
            }<br>
        }<br>

    }<br>
}<br>

**output**
![image](https://user-images.githubusercontent.com/98141713/150478977-e363ec57-9691-46e9-8c05-8a958e1f309f.png)


** Amicable number**

using System;<br>


    namespace Exercises<br>
{<br>
    class AmicableNumber<br>
    {<br>
        static void Main(string[] args)<br>
        {<br>


            int num1, num2, sum1 = 0, sum2 = 0;<br>
            Console.WriteLine("\n......AMICABLE NUMBERS........\n");<br>
            Console.WriteLine("\nEnter the first number:");<br>
            num1=Convert.ToInt32(Console.ReadLine());<br>
            Console.WriteLine("\nEnter the second number:");<br>
            num2 = Convert.ToInt32(Console.ReadLine());<br>

            for(int i=1;i<num1;i++)<br>
            {<br>
                if(num1%i==0)<br>
                {<br>
                    sum1 += i;<br>

                }<br>
            }<br>
            for(int i=1;i<num2;i++)<br>
            {<br>
                if (num2%i==0)<br>
                {<br>
                    sum2 += i;<br>

                }<br>

            }<br>
            if(sum1 == num2&&sum2==num1)<br>
            {<br>
                Console.WriteLine("\nThe numbers {0} and {1} are amicable.", num1, num2);<br>

            }<br>
            else<br>
            {
                Console.WriteLine("\nThe numbers {0} and {1} are not  amicable.", num1, num2);<br>
            }<br>
        }<br>
    }<br>
}<br>





**output**
![image](https://user-images.githubusercontent.com/98141713/150485296-e8e0dac3-9785-4af4-917d-a55753651552.png)


![image](https://user-images.githubusercontent.com/98141713/150485440-5b009ec1-5fcf-41f1-9bd4-ca6567433528.png)

**  c# program to illustrate the multilrvel inheritence with virtual method **
using System;
namespace Exercises
{
    class PersonalDetails
    {
        string name;
        int age;
        string gender;
        
        public PersonalDetails(string name,int age,string gender)
        {
            this.name = name;
            this.age = age;
            this.gender = gender;
        }
        public virtual void Display()
        {
            Console.WriteLine("\n------PERSONAL DETAILS-------\n");
            Console.WriteLine("Name=   :" + name);
            Console.WriteLine("Age=      :"+age);
            Console.WriteLine("Gender =    :" + gender);

        }


    }
    class CourceDetails : PersonalDetails
    {
        int regNo;
        string cource;
        int semester;

        public CourceDetails(string name, int age, string gender, int regNo, string cource,int semester):base(name,age,gender)
        {
            this.regNo = regNo;
            this.cource = cource;
            this.semester = semester;


        }
        public override void Display()
        {
            base.Display();
            Console.WriteLine("\n-------COURSE DETAILS-------\n");
            Console.WriteLine("Register Number     :" + regNo);
            Console.WriteLine("cource     :" + cource);
            Console.WriteLine("Semester     :" + semester);
        }
    }
    class MarksDetails : CourceDetails
    {
        int[] marks = new int[5];
        int total;
        float average;
        string grade;
        int flagFail;

        public MarksDetails(string name, int age, string gender, int regNo, string cource, int semester, int[] marks) : base(name, age, gender, regNo, cource, semester)
        {
            total = 0;
            for (int i = 0; i < 5; i++)
            {
                this.marks[i] = marks[i];
                total += marks[i];

                if (marks[i] < 35)
                {
                    flagFail = 1;

                }
            }
            Calculate();
        }
        private void Calculate()
        {
            average = total / 5;

            if (flagFail == 1 || average < 40)
                grade = "Fail";
            else
                if (average >= 70)
                grade = "Distinction";
            else
                  if (average >= 60)
                grade = "First Class";
            else
                if (average >= 50)
                grade = "Second Class";
            else
                grade = "pass";
        }
            public  override void Display()
        {
            base.Display();
            Console.WriteLine("\n---------Mark Details--------\n");
            Console.WriteLine("Marks in 5 subjects");
            for (int i = 0; i < 5; i++)
                Console.WriteLine(marks[i] + "");
            Console.WriteLine();
            Console.WriteLine("Total    :" + total);
            Console.WriteLine("Average    :" + average);
            Console.WriteLine("Grade    :" + grade);    
        }

        }
    class MultiLevel
    {
        public static void Main (string[]args)
        {
            MarksDetails student1 = new MarksDetails("Abhi", 21, "Male", 2021000, "MCA", 5, new int[] { 77, 80, 98, 95, 90 });
            student1.Display();

        }

    }
        }

** output **
![image](https://user-images.githubusercontent.com/98141713/152288873-394a3d82-412c-4e12-b223-bb3648d18a41.png)

