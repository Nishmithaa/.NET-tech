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





**output**<br>

![image](https://user-images.githubusercontent.com/98141713/150485296-e8e0dac3-9785-4af4-917d-a55753651552.png)


![image](https://user-images.githubusercontent.com/98141713/150485440-5b009ec1-5fcf-41f1-9bd4-ca6567433528.png)<br>


**  c# program to illustrate the multilrvel inheritence with virtual method **
using System;<br>

namespace Exercises<br>

{<br>

    class PersonalDetails<br>

    {<br>

        string name;<br>

        int age;<br>

        string gender;<br>

        
        public PersonalDetails(string name,int age,string gender)<br>

        {<br>

            this.name = name;<br>

            this.age = age;<br>

            this.gender = gender;<br>

        }<br>

        public virtual void Display()<br>

        {<br>

            Console.WriteLine("\n------PERSONAL DETAILS-------\n");<br>

            Console.WriteLine("Name=   :" + name);<br>

            Console.WriteLine("Age=      :"+age);<br>

            Console.WriteLine("Gender =    :" + gender);<br>


        }<br>



    }<br>

    class CourceDetails : PersonalDetails<br>

    {<br>

        int regNo;<br>

        string cource;<br>

        int semester;<br>


        public CourceDetails(string name, int age, string gender, int regNo, string cource,int semester):base(name,age,gender)<br>

        {<br>

            this.regNo = regNo;<br>

            this.cource = cource;<br>

            this.semester = semester;<br>



        }<br>

        public override void Display()<br>

        {<br>

            base.Display();<br>

            Console.WriteLine("\n-------COURSE DETAILS-------\n");<br>

            Console.WriteLine("Register Number     :" + regNo);<br>

            Console.WriteLine("cource     :" + cource);<br>

            Console.WriteLine("Semester     :" + semester);<br>

        }<br>

    }<br>

    class MarksDetails : CourceDetails<br>

    {<br>

        int[] marks = new int[5];<br>

        int total;<br>

        float average;<br>

        string grade;<br>

        int flagFail;<br>


        public MarksDetails(string name, int age, string gender, int regNo, string cource, int semester, int[] marks) : base(name, age, gender, regNo, cource, semester)<br>

        {<br>

            total = 0;<br>

            for (int i = 0; i < 5; i++)<br>

            {<br>

                this.marks[i] = marks[i];<br>

                total += marks[i];<br>


                if (marks[i] < 35)<br>

                {<br>

                    flagFail = 1;<br>


                }<br>

            }<br>

            Calculate();<br>

        }<br>

        private void Calculate()<br>

        {<br>

            average = total / 5;<br>


            if (flagFail == 1 || average < 40)<br>

                grade = "Fail";<br>

            else<br>

                if (average >= 70)<br>

                grade = "Distinction";<br>

            else<br>

                  if (average >= 60)<br>

                grade = "First Class";<br>

            else<br>

                if (average >= 50)<br>

                grade = "Second Class";<br>

            else<br>

                grade = "pass";<br>

        }<br>

            public  override void Display()<br>

        {<br>

            base.Display();<br>

            Console.WriteLine("\n---------Mark Details--------\n");<br>

            Console.WriteLine("Marks in 5 subjects");<br>

            for (int i = 0; i < 5; i++)<br>

                Console.WriteLine(marks[i] + "");<br>

            Console.WriteLine();<br>

            Console.WriteLine("Total    :" + total);<br>

            Console.WriteLine("Average    :" + average);<br>

            Console.WriteLine("Grade    :" + grade);    <br>

        }<br>


        }<br>

    class MultiLevel<br>

    {<br>

        public static void Main (string[]args)<br>

        {<br>

            MarksDetails student1 = new MarksDetails("Abhi", 21, "Male", 2021000, "MCA", 5, new int[] { 77, 80, 98, 95, 90 });<br>

            student1.Display();<br>



        }<br>


    }<br>

        }<br>


** output **<br>

![image](https://user-images.githubusercontent.com/98141713/152288873-394a3d82-412c-4e12-b223-bb3648d18a41.png)<br>



** C3 program to create a Gray code **

using System;<br>

namespace Exercises<br>

{<br>

    class GrayCode<br>

    {<br>

        static int getGray(int n)<br>

        {<br>

            return n^(n>>1);<br>


        }<br>

        static void Main (string[]args)<br>

        {<br>

            int inputNum,GrayNum;<br>

            Console.Write("\n Enter Decimal no:");<br>

            inputNum = Convert.ToInt32(Console.ReadLine());<br>


            Console.WriteLine("\n Binary equivalent of {0} :{1} " ,inputNum,<br>

                Convert.ToString(inputNum,2));<br>


            GrayNum=getGray(inputNum);<br>

            Console.WriteLine("\n Binary equivalent of {0} :{1} ", inputNum,<br>

               Convert.ToString(GrayNum, 2));<br>

        }<br>



    }<br>

}<br>

** output **<br>

![image](https://user-images.githubusercontent.com/98141713/152290932-fdff9ca7-0b2b-4f13-9c43-31375a94caae.png)



**6. Delegates **

using System;<br>

namespace Exercises<br>

{<br>

    class Delegates<br>

    {<br>

        delegate string UppercaseDelegate(string input);<br>

        static string UppercaseFirst(string input)<br>

        {<br>

        char[]buffer = input.ToCharArray();<br>

        buffer[0] = char.ToUpper(buffer[0]);<br>

        return new string (buffer);<br>

       }<br>

    static string UppercaseLast(string input)<br>

    {<br>

        char[] buffer = input.ToCharArray();<br>

        buffer[buffer.Length - 1] = char.ToUpper(buffer[buffer.Length - 1]);<br>

        return new string(buffer);<br>

    }<br>

    static string UppercaseAll(string input)<br>

    {<br>

        return input.ToUpper();<br>


    }<br>

    static void WriteOutput(string input,UppercaseDelegate del)<br>

    {<br>

        Console.WriteLine("Input String:{0}",input);<br>

        Console.WriteLine("Output String:{0}", del(input));<br>


       
    }<br>

    static void Main()<br>

    {<br>

        WriteOutput("tom",new UppercaseDelegate(UppercaseFirst));<br>

        WriteOutput("tom",new UppercaseDelegate(UppercaseLast));<br>

        WriteOutput("tom",new UppercaseDelegate(UppercaseAll));<br>

        Console.ReadLine();<br>


    }<br>

   }<br>


}<br>

**output**<br>

![image](https://user-images.githubusercontent.com/98141713/152299966-d3fc2e0e-a61a-484d-b050-033161f5f30f.png)


**%.Boxes **
using System;<br>

namespace Exercises<br>

{<br>

    class Box<br>

    {<br>

        float width;<br>

        float height;<br>

        float length;<br>


        public float volume<br>

        {<br>

            get { return width * height * length; }<br>

        }<br>


        public Box(float width, float height, float length)<br>

        {<br>

            this.width = width;<br>

            this.height = height;<br>

            this.length = length;<br>


        }<br>

        public static float operator +(Box box1, Box box2)<br>

        {<br>

            return box1.volume + box2.volume;<br>

        }<br>

        public override string ToString()<br>


        {<br>

            return "box with width " + width + ",height " + height + ",length " + length;<br>

        }<br>

    }<br>

    class operatorOverloading<br>

    {<br>

        public static void Main()<br>

        {<br>

            Box box1 = new Box(10, 20, 30);<br>

            Box box2 = new Box(25, 32, 15);<br>


            Console.WriteLine("Volume of {0} is :{1}", box1, box1.volume);<br>

            Console.WriteLine("Volume of {0} is :{1}", box2, box2.volume);<br>

            Console.WriteLine("Volume after adding boxes:{0}", box1 + box2);<br>


        }<br>


    }<br>

}<br>


**output **<br>

![image](https://user-images.githubusercontent.com/98141713/152300402-c9058078-be72-4302-98d5-c4159b057512.png)


** Freaquency of the word  **<br>

using System;<br>

namespace Exercises<br>

{<br>

    class FreaquencyIS<br>

    {<br>

        static void Main(string[]args)<br>

        {<br>

            int count = 0;<br>

            string inputString;<br>

            Console.WriteLine("\n----Freaquency of a word 'is'--------");<br>

            Console.WriteLine("\n Enter the input string:");<br>

            inputString = Console.ReadLine();<br>

            char[] seperator = { ',', ' ', '.', '!', '\n' };<br>

            string testString=inputString.ToLower();<br>

            String[]outcomes=testString.Split(seperator);<br>


            foreach(String s in outcomes)<br>

            {<br>

                Console.WriteLine(s);<br>

                if (s=="is")<br>

                    count++;<br>


            }<br>

            Console.WriteLine("\n Number of 'is' in '"+inputString+"'is:"+count);<br>


        }<br>

    }<br>

}<br>

** out put**<br>

![image](https://user-images.githubusercontent.com/98141713/152477756-bfb2a38f-4b5f-46fe-aab6-142c1b47fffe.png)


** Generate register number of student using static constructor **<br>

using System;<br>

namespace Exercises<br>

 {<br>

 class RegisterNum<br>

  {<br>

    int regNo;<br>

    static int startNum;<br>


    static RegisterNum()<br>

    {<br>

        startNum = 20210000;<br>


    }<br>

    RegisterNum()<br>

    {<br>

        regNo = ++startNum;<br>

    }<br>

    public static void Main(string[]args)<br>

    {<br>

        for(int i=0;i<100;i++)<br>

        {<br>

            RegisterNum Student = new RegisterNum();<br>

            Console.WriteLine("Student {0} :{1}",i+1,Student.regNo);<br>

        }<br>

    }<br>


  }<br>


}<br>

** output**<br>

![image](https://user-images.githubusercontent.com/98141713/152477244-f56272e9-912f-4b0d-bca6-2c48836f3405.png)
![image](https://user-images.githubusercontent.com/98141713/152477327-19876410-1ab1-436e-b6ab-48d144e92c13.png)
![image](https://user-images.githubusercontent.com/98141713/152477394-eac76e2a-c9af-439b-beff-db5ab7dff7ad.png)

** 2D ,jagged array Allocation **<br>
using System;<br>


using System.Diagnostics;<br>

namespace Exercises<br>

{<br>

    class BenchmarkAllocation<br>

    {<br>

        const int _max= 100000;<br>

        static void Main(string[] args)<br>

        {<br>

            var Arr2D = new int[100, 100];<br>

            var ArrJagged = new int[100][];<br>

            for (int i = 0; i < 100; i++)<br>

            {<br>

                ArrJagged[i] = new int[100];<br>

            }<br>

            var Stopwatch2D = Stopwatch.StartNew();<br>

            for (int i = 0; i < _max; i++)<br>

            {<br>

                for (int j = 0; j < 100; j++)<br>

                {<br>

                    for (int k = 0; k < 100; k++)<br>

                    {<br>

                        Arr2D[j, k] = k;<br>


                    }<br>

                }<br>

            }<br>

            Stopwatch2D.Stop();<br>

            var StopwatchJagged = Stopwatch.StartNew();<br>

            for (int i = 0; i <_max; i++)<br>

            {<br>

                for (int j = 0; j < 100; j++)<br>

                {<br>

                    for (int k = 0; k < 100; k++)<br>

                    {<br>

                        ArrJagged[j][k] = k;<br>


                    }<br>

                }<br>

            }<br>

            StopwatchJagged.Stop();<br>

            Console.Write("\n Time taken for Allocation in case of 2D array:");<br>

            Console.WriteLine(Stopwatch2D.Elapsed.TotalMilliseconds + "milliseconds");<br>

            Console.Write("\n Time taken for Allocation in case of jaggedarray:");<br>

            Console.WriteLine(StopwatchJagged.Elapsed.TotalMilliseconds + "milliseconds");<br>

        }<br>

    }<br>

}<br>


** Out put **<br>

![image](https://user-images.githubusercontent.com/98141713/152479926-933fe057-3f45-4bd4-9b93-96ad432b12a3.png)

** Sum of Diagonal matrix**<br>

using System;<br>

namespace Exercises<br>

{<br>

    class SumOfDiagonals<br>

    {<br>

        static void Main(string[]args)<br>

        {<br>

            int MaxRow, MaxCol, sum = 0;<br>

            int[,] Matrix;<br>


            Console.WriteLine("\n------Sum of diagonal matrix--------\n");<br>

            Console.Write("\n Enter the number in rows:");<br>

            MaxRow = Convert.ToInt32(Console.ReadLine());<br>

            Console.Write("\n Enter the number of columns:");<br>

            MaxCol = Convert.ToInt32(Console.ReadLine());<br>


            if (MaxRow != MaxCol)<br>

            {<br>

                Console.WriteLine("\n The Dimensiond entered is not a square matrix.");<br>

                Console.WriteLine("\n Exiting the program");<br>

                return;<br>

            }<br>

            Matrix = new int[MaxRow, MaxCol];<br>

            for (int i = 0; i < MaxRow; i++)<br>

            {<br>

                for (int j = 0; j < MaxCol; j++)<br>

                {<br>

                    Console.Write("\n Enter the ({0},{1}) th element of the the matrix :", (i + 1), (j + 1));<br>

                    Matrix[i, j] = Convert.ToInt32(Console.ReadLine());<br>

                }<br>

            }<br>

            Console.WriteLine("\n the entered matrix is:");<br>

            for (int i = 0; i < MaxRow; i++)<br>

            {<br>

                for (int j = 0; j < MaxCol; j++)<br>

                {<br>

                    Console.Write(" " + Matrix[i, j]);<br>

                    if (i == j)<br>

                    {<br>

                        sum += Matrix[i, j];<br>


                    }<br>

                }<br>

                Console.WriteLine();<br>

            }<br>

            Console.WriteLine("\n The sum of diagonal is" + sum);<br>


        }<br>


    }<br>

}<br>


**Output**<br>

![image](https://user-images.githubusercontent.com/98141713/152483570-2b18e10c-a709-402f-a4d8-316f7ca19e60.png)


** Create ,check the existence and read the contemts of the files **<br>

using System;<br>

using System.IO;<br>


namespace Exercises<br>

{<br>

    class FileRead<br>

    {<br>

        public static void Main()<br>

        {
            string fileName;<br>

            while(true)<br>

            {<br>

                Console.WriteLine("\n---------MENU----------\n");<br>

                Console.WriteLine("\n 1.Create a File");<br>

                Console.WriteLine("\n 2. Existence of the file");<br>

                Console.WriteLine("\n 3.Read the contents of the file");<br>

                Console.WriteLine("\n 4. Exit");<br>

                Console.WriteLine("\n Enter your choice: ");<br>

                int ch= int.Parse(Console.ReadLine());<br>

                switch(ch)<br>

                {<br>

                    case 1:<br>

                        Console.Write("\n Enter the File name to create:");<br>

                        fileName =Console.ReadLine();<br>

                        Console.WriteLine("\n Write the contents of the file:\n");<br>

                        string r = Console.ReadLine();<br>

                        using(StreamWriter fileStr = File.CreateText(fileName))<br>

                        {<br>

                            fileStr.WriteLine(r);<br>

                        }<br>

                        Console.WriteLine("File Created...");<br>

                        break;<br>


                        case 2:<br>

                        Console.Write("\n Enter the file name");<br>

                        fileName=Console.ReadLine();<br>

                        if(File.Exists(fileName))<br>

                        {<br>

                            Console.WriteLine("File Exists");<br>

                        }<br>

                        else<br>

                        {<br>

                            Console.WriteLine("File does not exist inthe current directory!");<br>


                        }<br>

                        break;<br>


                    case 3:<br>

                        Console.Write("\n Enter the file name to read the content:\n");<br><br>
                       
                        fileName = Console.ReadLine();<br>
                        if (File.Exists(fileName))<br>
                        {<br>
                            using (StreamReader sr = File.OpenText(fileName))<br>
                            {<br>
                                string s = "";<br>
                                Console.WriteLine("Here is the content of the fileL:");<br>
                                while((s=sr.ReadLine())!=null)<br>
                                {<br>
                                    Console.WriteLine(s);<br>

                                }<br>
                                Console.WriteLine("");<br>

                            }<br>
                        }<br>
                        else<br>
                        {<br>
                            Console.WriteLine("File does not exists");<br>
                        }<br>
                        break;<br>
                    case 4:<br>
                        Console.WriteLine("\n Exiting.....");<br>
                        return;<br>

                    default:<br>
                        Console.WriteLine("\n Invalid Choice");<br>
                        break;<br>

                }<br>

            }<br>
        }<br>
    }<br>
}<br>
** Output**<br>


![image](https://user-images.githubusercontent.com/98141713/152488263-e6a61ca3-5d78-46e1-ac3a-b74f246a9739.png)<br>
![image](https://user-images.githubusercontent.com/98141713/152488296-32ea9805-2364-40be-bd56-393d0c401056.png)<br>


**File comparision**

using System;
using System.IO;
namespace Exercises
{
    class FileRead
    {
        public static void Main()
        {
            string file1;
            string file2;

            Console.Write("Enter the first file path:");
            file1 = Console.ReadLine();

            Console.Write("Enter the second path:");
            file2 = Console.ReadLine();

            if (!File.Exists(file1))
            {
                Console.WriteLine("First file does not exist");

            }
            if (!File.Exists(file2))
            {
                Console.WriteLine("Second file does not exist");

            }

            else if (File.ReadAllText(file1) == File.ReadAllText(file2))
            { 

                Console.WriteLine("Both files contain the same content");
            }
            else
            {
                Console.WriteLine("Contents of the files are not same");

            }


        }
    }
}

   **output**
   ![image](https://user-images.githubusercontent.com/98141713/154415883-cd023d25-a835-4ebc-9bfa-00b0c56861c3.png)
   ![image](https://user-images.githubusercontent.com/98141713/154416193-164b7553-efde-416d-8941-0251c40a6d7a.png)
   

