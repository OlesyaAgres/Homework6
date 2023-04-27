# Homework6
// Практическое задание 6

// Задача 41: Пользователь вводит с клавиатуры M чисел. Посчитайте, сколько чисел больше 0 ввёл пользователь.

string ReadDataStr(string msg)
{
    Console.WriteLine(msg);
    return Console.ReadLine() ?? "0";
}

int CountPositivNumber(string str)
{
    int count = 0;
    string strWoSp = str.Replace(" ", "");

    string[] strArr = strWoSp.Split(",");

    int[] intArr = new int[strArr.Length];

    for (int i = 0; i < intArr.Length; i++) intArr[i] = int.Parse(strArr[i]);

    for (int i = 0; i < intArr.Length; i++) if (intArr[i] > 0) count++;

    return count;
}
string sequenceNumbers = ReadDataStr("Введите последовательность чисел: ");
int countPosNum = CountPositivNumber(sequenceNumbers);
Console.WriteLine("Количество положительных чисел равно: " + countPosNum);



//Задача 43: Напишите программу, которая найдёт точку пересечения двух прямых, заданных уравнениями 
// y = k1 * x + b1, y = k2 * x + b2; значения b1, k1, b2 и k2 задаются пользователем.

// double ReadData(string msg)
// {
//     Console.WriteLine(msg);
//     return Convert.ToDouble(Console.ReadLine() ?? "0");
// }
// 
// double xVolume(double b1, double k1, double b2, double k2)
// {
//     double xVol = (b2 - b1) / (k1 - k2);
//     //double x = (b2 - b1) / (k1 - k2);
//     return xVol;
// }

// double yVolume(double b1, double k1, double x)
// {
//     double y = k1 * x + b1;
//     return y;
// }

// double b1 = ReadData("Введите значение b1: ");
// double k1 = ReadData("Введите значение k1: ");
// double b2 = ReadData("Введите значение b2: ");
// double k2 = ReadData("Введите значение k2: ");

// double x = xVolume(b1, k1, b2, k2);
// double y = yVolume(b1, k1, x);

// Console.WriteLine("Значение Х = " + x);
// Console.WriteLine("Значение Y = " + y);

// вариант 2

// Console.WriteLine("введите значение b1");
// double b1 = Convert.ToInt32(Console.ReadLine());
// Console.WriteLine("введите число k1");
// double k1 = Convert.ToInt32(Console.ReadLine());
// Console.WriteLine("введите значение b2");
// double b2 = Convert.ToInt32(Console.ReadLine());
// Console.WriteLine("введите число k2");
// double k2 = Convert.ToInt32(Console.ReadLine());
// 
// double x = (-b2 + b1)/(-k1 + k2);
// double y = k2 * x + b2;
// 
// Console.WriteLine($"две прямые пересекутся в точке с координатами X: {x}, Y: {y}");


