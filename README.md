# Factorial1
class PROBLEMAFACTORIAL
	{

		public void OPERACION()
		{
			Random rando = new Random();
			int num = 6;
			int[] vec = new int[num];

			for (int a = 0; a < num; a++)
			{
				Console.WriteLine("NUMEROS:");
				vec[a] = rando.Next(2, 9);
				Console.WriteLine(vec[a]);
			}
			for (int a = 0; a < num; a++)
			{
				vec[a] = vec[a] * a;
				Console.WriteLine("EL NUMERO FACTORIAL ES: " + vec[a]);
			}
		}

		public int OPERACIONFACTORIAL(int n)
		{

			if (n == 0)
			{
				return 1;
			}
			else
			{
				return n + OPERACIONFACTORIAL(n - 1);
			}
		}
		static void Main(string[] args)
		{
			PROBLEMAFACTORIAL c = new PROBLEMAFACTORIAL();
			Random c2 = new Random();
            int op = 0;
			while (op != 9)
			{
				Console.WriteLine("1.- OPERACION FOR. ");
				Console.WriteLine("2.-OPERACION RECURSIVIDAD.");
				op = int.Parse(Console.ReadLine());
				Console.Clear();
				switch (op)
				{
					case 1:
						TimeSpan stop;
						TimeSpan start = new TimeSpan(DateTime.Now.Ticks);
						c.OPERACION();
						stop = new TimeSpan(DateTime.Now.Ticks);
						Console.Write(stop.Subtract(start).TotalSeconds); Console.WriteLine(" Segundos ");
						break;
					case 2:
                        
						
						TimeSpan starte = new TimeSpan(DateTime.Now.Ticks);
                        int FAC = c.OPERACIONFACTORIAL(8);
						Console.WriteLine("EL RESULTADO ES:" "+ ""+ FAC);
						stop = new TimeSpan(DateTime.Now.Ticks);
						Console.Write(stop.Subtract(start).TotalSeconds); Console.WriteLine(" Segundos ");
						break;
				}
			}
			Console.ReadKey();
		}
	}
