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
