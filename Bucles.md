# Bucles en C#

En programación utilizamos bucles para iterar la ejecución de uno o varios bloques de código dependiendo de una condición establecida según el tipo de bucle que se usa en el programa.

## Bucle while

El bucle más común es el bucle while, si la condición es verdadera el bloque de código se ejecutará en infinitas iteraciones mientras la condición sea verdadera, si es falsa se detendrá, por lo que el bucle while se utiliza cuando no se sabe exactamente la cantidad de veces que se va a iterar el bloque de código en cuestión.

SÍNTAXIS:
```C#
while (condición)
{
   // bloque de código que se ejecutará
}
```
EJEMPLO:

En el siguiente ejemplo el usuario va a una taquería para saciar su hambre comiendo tacos hasta que le indique que está satisfecho utilizando un "si" o "no" como respuesta, como extra se agregó un contador de tacos consumidos para contar la cantidad de iteraciones del bloque de código. 
```C#
using System;
namespace BucleWhile
{
    class Program
    {
        static void Main(string[] args)
        {
            //número de veces que se va a iterar el código dentro del while
            int TacosConsumidos = 0;

            Console.WriteLine("tienes hambre?");

            string respuesta = Console.ReadLine();

            //la condición es que siempre que el contenido del String "respuesta" sea "si" lo que está dentro de los corchetes del while seguirá iterando hasta que el usuario escriba otra cosa finalizando con el bucle

            while (respuesta == "si") 
            {
                Console.WriteLine("*come un taco*");

                TacosConsumidos++;

                Console.WriteLine("deseas comer más?");
                respuesta = Console.ReadLine();

                //aquí si el usuario escribió otra cosa que no haya sido si, el bucle terminará
            }
            Console.WriteLine($"consumiste {TacosConsumidos} tacos");
        }
    }
    
}
```
## Bucle do-while

La sentencia do-while funciona prácticamente igual al while con la importante diferencia de que el *while* **primero** evalúa la condición y **después** ejecuta el bloque de código, el *do-while* lo hace alrevés, **primero** ejecuta el bloque de código y **después** evalúa la condición.

SÍNTAXIS:
```C#
do
{
    // bloque de código que se ejecutará

}while (condición);
```
EJEMPLO:

El ejemplo es el mismo que el de while pero esta vez usando *do-while*.

```C#
using System;

namespace BucleWhile
{
    class Program
    {
        static void Main(string[] args)
        {
            int TacosConsumidos = 0;

            Console.WriteLine("tienes hambre?");

            string respuesta = Console.ReadLine();

            //primero ejecutará el codigo incluso si la condición es falsa
            do
            {
                Console.WriteLine("*come un taco*");
                TacosConsumidos++;
                Console.WriteLine("deseas comer más?");
                respuesta = Console.ReadLine();
            }
            //luego evalúa la condición para determinar si el do-while va a seguir iterando o no
            while (respuesta == "si");

            Console.WriteLine($"consumiste {TacosConsumidos} tacos");
        }
    }
    
}
```
## Bucle for

La sentencia de bucle *for* se suele utilizar cuando sabemos el número específico de iteraciones que necesitamos que se realicen dentro del bloque de código, declarando una **variable de inicialización**, un **límite de iteraciones** y un **contador incrementador o decrementador** como se muestra en la síntaxis más adelante.

SÍNTAXIS:

```C#
for (int i = 0 ; i <= x; i++)
{    
    //bloque de código que se ejecutará
}
```
EJEMPLO:
En el siguiente ejemplo se utiliza la sentencia de bucle *for* para imprimir un texto **6** veces, la variable *i* empieza con valor cero y va aumentando su valor +1 por cada iteración del bloque de código hasta llegar hasta el *6*. 

```C#
using System;

namespace BucleFor
{
    class Program
    {
        static void Main(string[] args)
        {
            for (int i = 0; i < 6; i++)
            {
                Console.WriteLine("TEXTO DE EJEMPLO");
            }
        }
    }
    
}
```

