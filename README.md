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

