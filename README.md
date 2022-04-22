 ****List Of .NET programmes****<br>
**1. Program to print Binary triangle**<br>
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


**Program to  check the entered number is Amicable number or not**

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


**c# program to illustrate the multilrvel inheritence with virtual method**<br>
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


**output**<br>

![image](https://user-images.githubusercontent.com/98141713/152288873-394a3d82-412c-4e12-b223-bb3648d18a41.png)<br>



**C3 program to create a Gray code **

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



**Program to implement the principlles of Delegates **

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


**Calaculate the volume of 2 Boxes and find the resultant volume  after adding the volume **
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


**Program to check Freaquency of the word 'is' **<br>

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


**Generate register number of student using static constructor **<br>

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

**program to bench mark 2D ,jagged array Allocation**<br>
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


**Out put**<br>

![image](https://user-images.githubusercontent.com/98141713/152479926-933fe057-3f45-4bd4-9b93-96ad432b12a3.png)

**Program to find the Sum of Diagonal matrix**<br>

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


**Create ,check the existence and read the contemts of the files **<br>

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
**Output**<br>


![image](https://user-images.githubusercontent.com/98141713/152488263-e6a61ca3-5d78-46e1-ac3a-b74f246a9739.png)<br>
![image](https://user-images.githubusercontent.com/98141713/152488296-32ea9805-2364-40be-bd56-393d0c401056.png)<br>


**Program to comparision of 2 files**

using System;<br>
using System.IO;<br>
namespace Exercises<br>
{<br>
    class FileRead<br>
    {<br>
        public static void Main()<br>
        {<br>
            string file1;<br>
            string file2;<br>

            Console.Write("Enter the first file path:");<br>
            file1 = Console.ReadLine();<br>

            Console.Write("Enter the second path:");<br>
            file2 = Console.ReadLine();<br>

            if (!File.Exists(file1))<br>
            {<br>
                Console.WriteLine("First file does not exist");<br>

            }<br>
            if (!File.Exists(file2))<br>
            {<br>
                Console.WriteLine("Second file does not exist");<br>

            }<br>

            else if (File.ReadAllText(file1) == File.ReadAllText(file2))<br>
            { <br>

                Console.WriteLine("Both files contain the same content");<br>
            }<br>
            
           
            else<br>
            {<br>
                Console.WriteLine("Contents of the files are not same");<br>

            }<br>


        }<br>
    }<br>
}<br>

   **output**<br>
   ![image](https://user-images.githubusercontent.com/98141713/154415883-cd023d25-a835-4ebc-9bfa-00b0c56861c3.png)<br>
   ![image](https://user-images.githubusercontent.com/98141713/154416193-164b7553-efde-416d-8941-0251c40a6d7a.png)<br>
   

**program to Implement Icomprable interface**<br>
using System;<br>
namespace Exercises<br>
{<br>
    class Fraction : IComparable<br>
    {<br>
        int z, n;<br>
        public Fraction(int z, int n)<br>
        {<br>
            this.z = z;<br>
            this.n = n;<br>
        }<br>
        public static Fraction operator +(Fraction a, Fraction b)<br>
        {<br>
            return new Fraction(a.z * b.n + a.n * b.z, a.n * b.n);<br>
        }<br>
        public static Fraction operator *(Fraction a, Fraction b)<br>
        {<br>
            return new Fraction(a.z * b.z, a.n * b.n);<br>
        }<br>
        public int CompareTo(object obj)<br>
        {<br>
            Fraction f = (Fraction)obj;<br>
            if ((float)z / n < (float)f.z / f.n)<br>
                return -1;<br>
            else if ((float)z / n > (float)f.z / f.n)<br>
                return 1;<br>
            else<br>
                return 0;<br>
        }<br>
        public override string ToString()<br>
        {<br>
            return z + "/" + n;<br>
        }<br>
    }<br>
    class ICompInterface<br>
    {<br>
        public static void Main()<br>
        {<br>

            Fraction[] a = {<br>
new Fraction(5,2),<br>
new Fraction(29,6),<br>
new Fraction(4,5),<br>
new Fraction(10,8),<br>
new Fraction(34,7)<br>
};<br>
            Array.Sort(a);<br>
            Console.WriteLine("Implementing the IComparable Interface in " + "Displaying Fractions : ");<br>
            foreach (Fraction f in a)<br>
            {<br>
                Console.WriteLine(f + " ");<br>
            }<br>
            Console.WriteLine();<br>
            Console.ReadLine();<br>
        }<br>
    }<br>
}<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/154419378-72aa804c-184c-4bbf-b538-5f053bbf1a5b.png)<br>


**Program to Create thread pools**<br>
using System;<br>
using System.Threading;<br>
namespace Exercises<br>
{<br>
    class ThreadPoolProg<br>
    {<br>
        public void ThreadFun1(object obj)<br>
        {<br>
            int loop = 0;<br>
            for (loop = 0; loop <= 4; loop++)<br>
            {<br>
                Console.WriteLine("Thread1 is executing");<br>
            }<br>
        }<br>
        public void ThreadFun2(object obj)<br>
        {<br>
            int loop = 0;<br>
            for (loop = 0; loop <= 4; loop++)<br>
            {<br>
                Console.WriteLine("Thread2 is executing");<br>
            }<br>
        }<br>
        public static void Main()<br>
        {<br>
            ThreadPoolProg TP = new ThreadPoolProg();<br>
            for (int i = 0; i < 2; i++)<br>
            {<br>
                ThreadPool.QueueUserWorkItem(new WaitCallback(TP.ThreadFun1));<br>
                ThreadPool.QueueUserWorkItem(new WaitCallback(TP.ThreadFun2));<br>
            }<br>
            Console.ReadKey();<br>
        }<br>
    }<br>
}<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/154424316-7d0bfec6-0978-4595-96ab-f402683ad75b.png)<br>

**Program to Demonstrate handling error using try catch method**<br>
using System;<br>
namespace Exercises<br>
{<br>
    class ExceptionHandling<br>
    {<br>
        static void Main(string[] args)<br>
        {<br>
            Age a = new Age();<br>
            try<br>
            {<br>
                a.displayAge();<br>
            }<br>
            catch (AgeIsNegativeException e)<br>
            {<br>
                Console.WriteLine("AgeIsNegativeException: {0}", e.Message);<br>
            }<br>
            finally<br>
            {<br>
                Console.WriteLine("Execution of Finally block is done.");<br>
            }<br>
        }<br>
    }<br>
}<br>
public class AgeIsNegativeException : Exception<br>
{<br>
    public AgeIsNegativeException(string message) : base(message)<br>
    {<br>
    }<br>
}<br>
public class Age<br>
{<br>
    int age = -5;<br>
    public void displayAge()<br>
    {<br>
        if (age < 0)<br>
        {<br>
            throw (new AgeIsNegativeException("Age cannot be negative"));<br>
        }<br>
        else<br>
        {<br>
            Console.WriteLine("Age is: {0}", age);<br>
        }<br>
    }<br>
}<br>
<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/154424933-596032b0-97f1-448f-a382-1ba9b1d70ea9.png)<br>


**C# program to print fibonacci number**<br>
using System;<br>
public class FibonacciExample<br>
{<br>
    public static void Main(string[] args)<br>
    {<br>
        int n1 = 0, n2 = 1, n3, i, number;<br>
        Console.Write("Enter the number of elements: ");<br>
        number = int.Parse(Console.ReadLine());<br>
        Console.Write(n1 + " " + n2 + " ");  <br>
        for (i = 2; i < number; ++i)    <br>
        {<br>
            n3 = n1 + n2;<br>
            Console.Write(n3 + " ");<br>
            n1 = n2;<br>
            n2 = n3;<br>
        }<br>
    }<br>
}<br>
**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155659583-553702b5-9b78-4f85-9050-8aaeff954ae7.png)<br>

**C# program to check whether entered number is prime or not**<br>
using System;<br>
public class PrimeNumberExample<br>
{<br>
    public static void Main(string[] args)<br>
    {<br>
        int n, i, m = 0, flag = 0;<br>
        Console.Write("Enter the Number to check Prime: ");<br>
        n = int.Parse(Console.ReadLine());<br>
        m = n / 2;<br>
        for (i = 2; i <= m; i++)<br>
        {<br>
            if (n % i == 0)<br>
            {<br>
                Console.Write("Not is not Prime.");<br>
                flag = 1;<br>
                break;<br>
            }<br>
        }<br>
        if (flag == 0)<br>
            Console.Write("Number is Prime.");<br>
    }<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155660567-d6e5c053-4a8e-4a4f-8a20-5bffba3bde58.png)<br>
![image](https://user-images.githubusercontent.com/98141713/155660665-e448aef8-82f2-4252-84de-7905bc161e05.png)<br>


**C# program to check whethe the entered number is palindrome or not.**<br><br>

using System;<br>
public class PalindromeExample<br>
{<br><br>
    public static void Main(string[] args)<br>
    {<br>
        int n, r, sum = 0, temp;<br>
        Console.Write("Enter the Number: ");<br>
        n = int.Parse(Console.ReadLine());<br>
        temp = n;<br>
        while (n > 0)<br>
        {<br>
            r = n % 10;<br>
            sum = (sum * 10) + r;<br>
            n = n / 10;<br>
        }<br>
        if (temp == sum)<br>
            Console.Write("Number is Palindrome.");<br>
        else<br>
            Console.Write("Number is not Palindrome");<br>
    }<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155661626-d0438f5e-ea44-49a0-ac02-b503253a037b.png)<br>
![image](https://user-images.githubusercontent.com/98141713/155661756-d96a69ee-f912-4ab1-ae5d-ea00f975d43d.png)<br>

**C# program to find the factorial of the number**<br>

using System;<br>
public class FactorialExample<br>
{<br>
    public static void Main(string[] args)<br>
    {<br>
        int i, fact = 1, number;<br>
        Console.Write("Enter any Number: ");<br>
        number = int.Parse(Console.ReadLine());<br>
        for (i = 1; i <= number; i++)<br>
        {<br>
            fact = fact * i;<br>
        }<br>
        Console.Write("Factorial of " + number + " is: " + fact);<br><br>
    }<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155662479-c356c2e3-f20f-45ca-a7be-88306b2b0e90.png)<br>

**C# program to check the armstrong number**<br>

using System;<br>
public class ArmstrongExample<br>
{<br>
    public static void Main(string[] args)<br>
    {<br>
        int n, r, sum = 0, temp;<br>
        Console.Write("Enter the Number= ");<br>
        n = int.Parse(Console.ReadLine());<br>
        temp = n;<br>
        while (n > 0)<br>
        {<br>
            r = n % 10;<br>
            sum = sum + (r * r * r);<br>
            n = n / 10;<br>
        }<br>
        if (temp == sum)<br>
            Console.Write("Armstrong Number.");<br>
        else<br>
            Console.Write("Not Armstrong Number.");<br>
    }<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155665893-e0365ce6-0844-4227-90b9-55f023170d69.png)<br>
![image](https://user-images.githubusercontent.com/98141713/155665984-5cc2ffd2-bf88-4722-a31a-835727e4d048.png)<br>

**C# program to check the sum of the numbers**<br>

using System;<br>
public class SumExample<br>
{<br>
    public static void Main(string[] args)<br>
    {<br>
        int n, sum = 0, m;<br>
        Console.Write("Enter a number: ");<br>
        n = int.Parse(Console.ReadLine());<br>
        while (n > 0)<br>
        {<br>
            m = n % 10;<br>
            sum = sum + m;<br>
            n = n / 10;<br>
        }<br>
        Console.Write("Sum is= " + sum);<br>
    }<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155667382-eb0a3d88-88ff-4613-85dc-8fda7124a346.png)<br>


**C# program to reverese a number**<br>

using System;<br>
public class ReverseExample<br>
{<br>
    public static void Main(string[] args)<br>
    {<br>
        int n, reverse = 0, rem;<br>
        Console.Write("Enter a number: ");<br>
        n = int.Parse(Console.ReadLine());<br>
        while (n != 0)<br>
        {<br>
            rem = n % 10;<br>
            reverse = reverse * 10 + rem;<br>
            n /= 10;<br>
        }<br>
        Console.Write("Reversed Number: " + reverse);<br>
    }<br>
}<br>

**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/155668185-182d6c4a-f5c3-414d-befe-998c5e3a4b05.png)<br>

**progress bar**
using System;<br>
using System.Collections.Generic;<br>
using System.ComponentModel;<br>
using System.Data;<br>
using System.Drawing;<br>
using System.Linq;<br>
using System.Text;<br>
using System.Threading;<br>
using System.Windows.Forms;<br>

namespace progress_bar<br>
{<br>
    public partial class Form1 : Form<br>
    {<br>
        public Form1()<br>
        {<br>
            InitializeComponent();<br>
        }<br>

       

        private void Form1_Load(object sender, EventArgs e)<br>
        {<br>
            
                backgroundWorker1.WorkerReportsProgress = true;<br>
                backgroundWorker1.RunWorkerAsync();<br>

        }<br>

        private void backgroundWorker1_DoWork(object sender, DoWorkEventArgs e)<br>
        {<br>
            
                for (int i = 1; i <= 100; i++)<br>
                {<br>
                    Thread.Sleep(50);<br>
                    backgroundWorker1.ReportProgress(i);<br>
                }<br>

        }<br>

        private void backgroundWorker1_ProgressChanged(object sender, ProgressChangedEventArgs e)<br>
        {<br>
            {<br>
                progressBar1.Value = e.ProgressPercentage;<br>
                this.Text = "progress:" + e.ProgressPercentage.ToString() + "%";<br>

            }<br>
        }<br>

        private void backgroundWorker1_RunWorkerCompleted(object sender, RunWorkerCompletedEventArgs e)<br>
        {<br>

        }<br>

       
    }<br>
}<br>


**Output**<br>
![image](https://user-images.githubusercontent.com/98141713/158751766-dbcd8540-1dbf-4f39-8833-6889c02e3389.png)<br>




**Guess the number**

using System;<br>
using System.Collections.Generic;<br>
using System.ComponentModel;<br>
using System.Data;<br>
using System.Drawing;<br>
using System.Linq;<br>
using System.Text;<br>
using System.Threading.Tasks;<br>
using System.Windows.Forms;<br>

namespace Guessss<br>
{<br>
    public partial class Form1 : Form<br>
    {<br>
        static Random r = new Random();<br>
        int value;<br>
        int guessnum;<br>
        int win = 10;<br>
        int guess = 1;<br>
        Button button1;<br>
        TextBox textBox1;<br>
        RichTextBox richTextBox1;<br>
        RichTextBox richTextBox2;<br>
        Label label4;<br>
        public Form1()<br>
        {<br>
            InitializeComponent();<br>
            value = r.Next(10);<br>
            this.Controls.Clear();<br>
            this.BackColor = Color.SkyBlue;<br>
            this.AutoSize = true;<br>
            this.Padding = new Padding(16);<br>

            Label label = new Label();<br>
            label.Text = "Pick a number between 1 and 10";<br>
            label.Bounds = new Rectangle(10, 20, 340, 40);<br>
            label.Font = new Font("Arial", 16);<br>
            textBox1 = new TextBox();<br>
            textBox1.Bounds = new Rectangle(20, 50, 120, 80);<br>
            textBox1.Font = new Font("Arial", 24);<br>
            button1 = new Button();<br>
            button1.Text = " Check Your Guess ";<br>
            button1.Bounds = new Rectangle(160, 50, 120, 40);<br>
            button1.BackColor = Color.LightGray;<br>
            button1.Click += new EventHandler(button1_Click);<br>
            Label label2 = new Label();<br>
            label2.Text = "Low Guess";<br>
            label2.Bounds = new Rectangle(20, 150, 160, 40);<br>
            label2.Font = new Font("Arial", 18);<br>
            richTextBox1 = new RichTextBox();<br>
            richTextBox1.Bounds = new Rectangle(20, 190, 160, 300);<br>
            richTextBox1.Font = new Font("Arial", 16);<br>
            Label label3 = new Label();<br><br>
            label3.Text = "High Guess";<br>
            label3.Bounds = new Rectangle(180, 150, 160, 40);<br>
            label3.Font = new Font("Arial", 18);<br>
            richTextBox2 = new RichTextBox();<br>
            richTextBox2.Bounds = new Rectangle(180, 190, 160, 300);<br>
            richTextBox2.Font = new Font("Arial", 16);<br>
            label4 = new Label();<br>
            label4.Bounds = new Rectangle(20, 100, 340, 40);<br>
            label4.Font = new Font("Arial", 16);<br>
            this.Controls.Add(label);<br>
            this.Controls.Add(textBox1);<br>
            this.Controls.Add(button1);<br>
            this.Controls.Add(label4);<br>
            this.Controls.Add(label2);<br>
            this.Controls.Add(label3);<br>
            this.Controls.Add(richTextBox1);<br>
            this.Controls.Add(richTextBox2);<br>
        }<br><br>
        private void button1_Click(object sender, EventArgs e)<br>
        {<br>
            // Coding of game 
            if (textBox1.Text == "")<br>
            {<br>
                return;<br>
            }<br>
            guessnum = Convert.ToInt32(textBox1.Text);<br>
            textBox1.Text = String.Empty;<br>
            if (win >= 0)<br><br>
            {<br>
                if (guessnum == value)<br>
                {<br>
                    MessageBox.Show("You have guessed the number! \n The number was " + value);<br>
                    InitializeComponent();<br>
                }<br>
                else if (guessnum < value)<br>
                {<br>
                    richTextBox1.Text += guessnum + "\n";<br>
                    MessageBox.Show("wrong Guess and number of guesses left are  " + (10 - guess));<br>

                }<br>
                else if (guessnum > value)<br>
                {<br>
                    richTextBox2.Text += guessnum + "\n";<br>
                    MessageBox.Show("wrong Guess and number of guesses left are  " + (10 - guess));<br>
                }<br>
                guess++;<br>
                win--;<br>
            }<br>
            if (guess == 11)<br>
            {<br>
                label4.Text = "You loose,Correct Guess is " + value;<br>
            }<br>
        }<br><br>
    }<br>
}<br>

**Output**
![image](https://user-images.githubusercontent.com/98141713/159851750-eaeacdea-ffdc-4e8a-97d6-0e0bb91e62ab.png)<br>

**Notepad**
using System;<br>
using System.Collections.Generic;<br>

using System.ComponentModel;

using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace notepad1
{
    public partial class Form1 : Form
    {
        private string fileName;
        private RichTextBox txtContent;
        private ToolBar toolBar;
        internal Form1()
        {
            fileName = null;
            InitializeComponents();
        }
        void InitializeComponents()
        {
            this.Text = "My notepad";
            this.MinimumSize = new Size(600, 450);
            this.FormClosing += new FormClosingEventHandler(NotepadClosing);
            this.MaximizeBox = true;
            toolBar = new ToolBar();
            toolBar.Font = new Font("Arial", 16);
            toolBar.Padding = new Padding(4);
            toolBar.ButtonClick += new ToolBarButtonClickEventHandler(toolBarClicked);
            ToolBarButton toolBarButton1 = new ToolBarButton();
            ToolBarButton toolBarButton2 = new ToolBarButton();
            ToolBarButton toolBarButton3 = new ToolBarButton();
            toolBarButton1.Text = "New";
            toolBarButton2.Text = "Open";
            toolBarButton3.Text = "Save";
            toolBar.Buttons.Add(toolBarButton1);
            toolBar.Buttons.Add(toolBarButton2);
            toolBar.Buttons.Add(toolBarButton3);
            txtContent = new RichTextBox();
            txtContent.Size = this.ClientSize;
            txtContent.Height -= toolBar.Height;
            txtContent.Top = toolBar.Height;
            txtContent.Anchor = AnchorStyles.Left | AnchorStyles.Right |
           AnchorStyles.Top | AnchorStyles.Bottom;
            txtContent.Font = new Font("Arial", 16);
            txtContent.AcceptsTab = true;
            txtContent.Padding = new Padding(8);

            this.Controls.Add(toolBar);
            this.Controls.Add(txtContent);
        }
        private void toolBarClicked(Object sender, ToolBarButtonClickEventArgs e)
        {
            saveFile();
            switch (toolBar.Buttons.IndexOf(e.Button))
            {
                case 0:
                    this.Text += "My notepad";
                    txtContent.Text = string.Empty;
                    fileName = null;
                    break;
                case 1:
                    OpenFileDialog openDlg = new OpenFileDialog();
                    if (DialogResult.OK == openDlg.ShowDialog())
                    {
                        fileName = openDlg.FileName;
                        txtContent.LoadFile(fileName);
                        this.Text = "My notepad " + fileName;
                    }
                    break;
            }
        }
        void saveFile()
        {
            if (fileName == null)
            {
                SaveFileDialog saveDlg = new SaveFileDialog();
                if (DialogResult.OK == saveDlg.ShowDialog())
                {
                    fileName = saveDlg.FileName;
                    this.Text += " " + fileName;
                }
            }
            else
            {
                txtContent.SaveFile(fileName, RichTextBoxStreamType.RichText);
            }
        }
        private void NotepadClosing(Object sender, FormClosingEventArgs e)
        {
            saveFile();
        }
        static void main(String[] args)
        {


            Application.Run(new Form1());
        }
    }

}

**Output**


using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Drawing.Drawing2D;


namespace WindowsFormsApp10
{
    public partial class Form1 : Form

    {
        private Node root;
        public Form1()
        {
            InitializeComponent();
            this.root = null;
            test();

        }
        void test()
        {
            textBox1.Text = "5";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "3";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "2";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "1";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "4";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "7";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "6";
            btnAdd_Click(btnAdd, null);
            textBox1.Text = "8";
            btnAdd_Click(btnAdd, null);
        }


        private void btnAdd_Click(object sender, EventArgs e)
        {
            int value = int.Parse(textBox1.Text);
            if (root == null)
                root = new Node(value);
            else

            {
                if (root.Add(value) == false)
                    MessageBox.Show("The value already exists!");

            }
            drawTree();

        }

        private void btnCreate_Click(object sender, EventArgs e)
        {
            root = null;
            pictureBox1.Image = null;
        }

        private void btnRemove_Click(object sender, EventArgs e)
        {
            int value = int.Parse(textBox1.Text);
            if (root != null)

            {
                bool status = root.Remove(value, root, ref root);
                if (status == false)

                {
                    MessageBox.Show("the value does not exists");

                }

            }
            drawTree();

        }

        private void btnSearch_Click(object sender, EventArgs e)
        {
            string msg;
            int value = int.Parse(textBox1.Text);
            if (root == null)

            {
                msg = "Tree is empty";
            }
            else

            {
                if (root.Exists(value))

                {
                    msg = "Value found";
                }
                else

                {
                    msg = "Value not found";

                }

            }
            MessageBox.Show(msg);

        }
        void drawTree()
        {
            if (root != null)
                pictureBox1.Image = root.Draw();
            else
                pictureBox1.Image = null;
            this.Update();
        }
        
    }
    class Node
    {
        internal Node left { get; set; }
        internal Node right { get; set; }
        internal int value;
        internal int center = 12;
        private static Bitmap nodeBg = new Bitmap(30, 25);
        private static Font font = new Font("Arial", 14);
        internal Node(int value)
        {
            this.value = value;
        }
        internal bool Add(int value)
        {
            Node node = new Node(value);
            if (value < this.value)
            {
                if (this.left == null)
                {
                    this.left = node;
                    return true;
                }
                else
                    return this.left.Add(value);
            }
            else if (value > this.value)
            {
                if (this.right == null)
                {
                    this.right = node;
                    return true;
                }
                else
                    return this.right.Add(value);
            }
            return false;
        }
        internal bool Remove(int value, Node parent, ref Node root)
        {
            if (value < this.value)
            {
                if (left != null)
                {
                    return left.Remove(value, this, ref root);
                }
            }
            else if (value > this.value)
            {
                if (right != null)
                {
                    return right.Remove(value, this, ref root);
                }
            }
            else if (value == this.value)
            {
                bool isLeft = (this == parent.left);
                if (left == null && right == null)
                {
                    if (root == this)
                        root = null;
                    else
                    if (isLeft) parent.left = null; else parent.right = null;
                }
                else if (right == null)
                {
                    if (isLeft) parent.left = left; else parent.right = left;
                    if (root == this)
                        root = left;
                }
                else
                {
                    if (right.left == null)
                    {
                        right.left = left;
                        if (isLeft) parent.left = right;
                        else
                            parent.right = right;
                        if (root == this)
                            root = right;
                    }
                    else
                    {
                        Node node = right;
                        while (node.left.left != null)
                            node = node.left;
                        Console.WriteLine("Node: " + node.value);
                        this.value = node.left.value;
                        Console.WriteLine("here");
                        node.left = null;
                    }
                }
                return true;
            }
            return false;
        }
        public Image Draw()
        {
            Size lSize = new Size(nodeBg.Width / 2, 0);
            Size rSize = new Size(nodeBg.Width / 2, 0);
            Image lNodeImg = null;
            Image rNodeImg = null;
            int lCenter = 0, rCenter = 0;

            if (this.left != null)
            {
                lNodeImg = left.Draw();
                lSize = lNodeImg.Size;
                this.center = lSize.Width;
                lCenter = left.center;<br>
            }<br>
            if (this.right != null)<br>
            {<br>
                rNodeImg = right.Draw();<br>
                rSize = rNodeImg.Size;<br>
                rCenter = right.center;<br>
            }<br>
            int maxHeight = (lSize.Height < rSize.Height) ? rSize.Height : lSize.Height;<br>
            if (maxHeight > 0) maxHeight += 35;<br>
            Size resultSize = new Size(lSize.Width + rSize.Width, nodeBg.Size.Height +<br>
maxHeight);<br>
            Bitmap result = new Bitmap(resultSize.Width, resultSize.Height);<br>

            Graphics g = Graphics.FromImage(result);<br>
            g.SmoothingMode = SmoothingMode.HighQuality;<br>
            g.FillRectangle(Brushes.White, new Rectangle(new Point(0, 0), resultSize));<br>
            g.DrawImage(nodeBg, lSize.Width - nodeBg.Width / 2, 0);<br>

            string str = "" + value;<br>
            g.DrawString(str, font, Brushes.Black, lSize.Width - nodeBg.Width / 2 + 7,<br>
           nodeBg.Height / 2f - 12);<br>
            Pen pen = new Pen(Brushes.Black, 1.2f);<br>
            float x1 = center;<br><br>
            float y1 = nodeBg.Height;<br><br>
            float y2 = nodeBg.Height + 35;<br><br>
            float x2 = lCenter;<br><br>
            var h = Math.Abs(y2 - y1);<br><br>
            var w = Math.Abs(x2 - x1);<br><br>
            if (lNodeImg != null)<br><br><br>
            {<br>
                g.DrawImage(lNodeImg, 0, nodeBg.Size.Height + 35);<br>
                var points1 = new List<PointF><br>
 {<br>
 new PointF(x1, y1),<br>
 new PointF(x1 - w/6, y1 + h/3.5f),<br>
 new PointF(x2 + w/6, y2 - h/3.5f),<br>
 new PointF(x2, y2),<br>
 };<br>
                g.DrawCurve(pen, points1.ToArray(), 0.5f);<br>
            }<br>
            if (rNodeImg != null)<br>
            {<br>
                g.DrawImage(rNodeImg, lSize.Width, nodeBg.Size.Height + 35);<br>
                x2 = rCenter + lSize.Width;<br>
                w = Math.Abs(x2 - x1);<br>
                var points = new List<PointF><br>
 {<br>
 new PointF(x1, y1),<br>
 new PointF(x1 + w/6, y1 + h/3.5f),<br>
 new PointF(x2 - w/6, y2 - h/3.5f),<br>
 new PointF(x2, y2)<br>
 };<br>
                g.DrawCurve(pen, points.ToArray(), 0.5f);<br>
            }<br>
            return result;<br>
        }<br>
        public bool Exists(int value)<br>
        {<br>
            bool res = value == this.value;<br>
            if (!res && left != null)<br>
                res = left.Exists(value);<br>
            if (!res && right != null)<br>
                res = right.Exists(value);<br>
            return res;<br>
          }<br>
        }<br>
}<br>
**output**
![image](https://user-images.githubusercontent.com/98141713/160989845-f9a7ce54-de58-4b5c-9490-92bb6970d31a.png)
