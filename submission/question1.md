static void Main(string[] args)
        {
            int[] arr = new int[] { 2, 3, 1, 4, 6, 9, 7, 8, 10, 7 };
            Array.Sort(arr);
            int cur = 0;
            for (int i = 0; i < arr.Length; i++)
            {
                if (arr[i] == cur + 1)
                {
                    cur = arr[i];
                }
                else
                {
                    int victim = arr[i] - 1;
                    Console.WriteLine("{0}", victim);
                    break;
                }
            }
            Console.WriteLine("End....");
        }