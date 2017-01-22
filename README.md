# Christmas-Hat
Програма, която прочита от конзолата цяло число N и чертае коледна шапка с ширина 4 * n + 1 колони и височина 2 * n + 5 реда 

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ChristmasHat
{
	class Program
	{
		static void Main(string[] args)
		{
			var n = int.Parse(Console.ReadLine());
			var firstLine = new string('.', 2 * n - 1) + "/" + "|" + "\\" + new string('.', 2 * n - 1);
			var secondLine = new string('.', 2 * n - 1) + "\\" + "|" + "/" + new string('.', 2 * n - 1);
			Console.WriteLine(firstLine);
			Console.WriteLine(secondLine);
			for (int i = 0; i <2* n; i++)
			{
				Console.Write(new string('.',2*n-i-1));
				Console.Write("*");
				Console.Write(new string('-',i));
				Console.Write("*");
				Console.Write(new string('-', i));
				Console.Write("*");
				Console.WriteLine(new string('.', 2*n-i - 1));
			}
			var last1 = new string('*', 4 * n + 1);
			var last2 = magicString("*.", 2 * n);
			var last3 = new string('*', 4 * n + 1);
			Console.WriteLine(last1);
			Console.WriteLine(last2 + "*");
			Console.WriteLine(last3);
		}
		public static string magicString(string text, int repeatCount)
		{
			string outputText = "";
			for (int i = 0; i < repeatCount; i++)
			{
				outputText=outputText+text;
			}
			return outputText;
		}
	}
}
