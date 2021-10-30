# seminario-1-de-EDA
using System;

namespace isercion_directa
{
    class insercion
    {
        private int[] lista;
        public void inicio()
        {
            Console.WriteLine("======================================");
            Console.WriteLine("Prueva de metodo de insercion directa ");
            Console.WriteLine("======================================");
            Console.Write("ingrese el tamaño de la lista: ");
            string lectura;
            lectura = Console.ReadLine();
            int tammano;
            tammano = int.Parse(lectura);
            lista = new int[tammano];
            Console.WriteLine("======================================");
            for (int i = 0; i < lista.Length; i++)
            {
                Console.Write("=ingrese el elemento No." + (i + 1) + ": ");
                lectura = Console.ReadLine();
                lista[i] = int.Parse(lectura);
            }
            Console.WriteLine("======================================");

        }
        public void InsercionDirecta()
        {
            int auxiliar;
            int w;
            for (int a = 0; a < lista.Length; a++)
            {
                auxiliar = lista[a];
                w = a - 1;
                while (w >= 0 && lista[w] > auxiliar)
                {
                    lista[w + 1] = lista[w];
                    w--;

                }
                lista[w + 1] = auxiliar;
            }

        }
        public void presentar()
        {
            Console.WriteLine("Llista ordenada Ascendente");
            for(int i= 0; i < lista.Length; i ++)
            {
                Console.WriteLine(lista[i] + " ");

            }
            Console.WriteLine("======================================");
            Console.ReadKey();
        }

        static void Main(string[] args)
        {
            insercion ing= new insercion();
            ing.inicio();
            ing.InsercionDirecta();
            ing.presentar();
        }

    }



    


}
