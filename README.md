namespace SEMANA_2_LISTAS_ENLAZADAS
{
    internal class Program
    {   

        public class Nodo
        {
            public int Dato;
            public Nodo Siguiente;
            
            public Nodo(int valor)
            {
                Dato = valor;
                Siguiente = null;
            }
            
        }
        static void Main(string[] args)
        {
            int num;
            Console.WriteLine("Ingrese un número entero: ");
            num = int.Parse(Console.ReadLine());

            int c = 1;
            Nodo n1 = new Nodo(10);
            Nodo n2 = new Nodo(20);
            Nodo n3 = new Nodo(30);
            Nodo n4 = new Nodo(40);
            Nodo n5 = new Nodo(50);
            Nodo n6 = new Nodo(60);
            Nodo n7 = new Nodo(70);
            Nodo n8 = new Nodo(80);
            Nodo n9 = new Nodo(90);
            Nodo n10 = new Nodo(100);

            Nodo cabeza = n1;
            n1.Siguiente = n2;
            n2.Siguiente = n3;
            n3.Siguiente = n4;
            n4.Siguiente = n5;
            n5.Siguiente = n6;
            n6.Siguiente = n7;
            n7.Siguiente = n8;
            n8.Siguiente = n9;
            n9.Siguiente = n10;

            /*
            Console.WriteLine("Nodo1 : " + cabeza.Dato);
            Console.WriteLine("Nodo2 : " + cabeza.Siguiente.Dato);
            Console.WriteLine("Nodo3 : " + cabeza.Siguiente.Siguiente.Dato);
            Console.WriteLine("Nodo4 : " + cabeza.Siguiente.Siguiente.Siguiente.Dato);
            Console.WriteLine("Nodo5 : " + cabeza.Siguiente.Siguiente.Siguiente.Siguiente.Dato);
            Console.WriteLine("Nodo6 : " + cabeza.Siguiente.Siguiente.Siguiente.Siguiente.Siguiente.Dato);
            */

            //BUCLE WHILE

            Nodo actual = cabeza;

            while (actual != null)
            {
                Console.WriteLine("Nodo " + c +":"+ actual.Dato);
                actual = actual.Siguiente;
                c++;
            }
       
            if(n10.Siguiente == null)
            {
                Console.WriteLine("FIN DE LA LISTA (NULL)");
            }
        }
    }
}
