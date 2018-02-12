# Examen SI-401
Tema 1. Recursividad Fibonacci

La recursividad, es un concepto bastante importante y bien básico de la programación. Sin embargo es bastante difícil de asimilar 
al principio. Se supone que es algo que se va entendiendo con práctica y tiempo.

1. Ejemplo en java:

package calculofibonacci;

public class CalculoFibonacci{
 public long fibonacci( long numero ) {
     if ( ( numero == 0 ) || ( numero == 1 ) ) // casos base
         return numero;
     else // paso recursivo
         return fibonacci( numero - 1 ) + fibonacci( numero - 2 );
 } 
 public void mostrarFibonacci()
 {
 for ( int contador = 0; contador <= 16; contador++ )
 System.out.printf( "Fibonacci de %d es: %d\n", contador,
 fibonacci( contador ) );
 }
}
//Objeto main
package calculofibonacci;


public class PruebaFibonacci{
    public static void main( String args[] ){        
        CalculoFibonacci calculoFibonacci = new CalculoFibonacci();
            calculoFibonacci.mostrarFibonacci();
 }
 }
 
2. Ejemplo en python:

sucesion = input("Ingrese: (S) límite máximo, (N) número de \
términos? ")

if sucesion == 'S':
    def fib(n):
        a, b = 0,1
        while a < n:
            print(a, end=' ')
            a, b = b, a + b
    m = int(input("Límite máximo~> "))   
    fib(m)

elif sucesion == 'N':
    a, b = 0,1
    n = int(input("Número de términos~> "))
    for i in range(n):
        print(i, a)
        a, b = b, a + b

else:
    print("Debe ingresar S o N")

Tema 2. Recursividad Factorial

1. Ejemplo en java:

package calculofactorial;
public class CalculoFactorial{
public long factorial( long numero ){
     if ( numero <= 1 )
           return 1;
     else
 return numero * factorial( numero - 1 );
 } 
 public void mostrarFactoriales(){
     
 for ( int contador = 0; contador <= 16; contador++ )
 System.out.printf( "%d! = %d\n", contador, factorial( contador ) );
 }
 }
 
 //Estecodigo es para correr el programa
 package calculofactorial;
public class PruebaFactorial{
    
public static void main( String args[] ){
    
CalculoFactorial calculoFactorial = new CalculoFactorial();
 calculoFactorial.mostrarFactoriales();
 }
 } 
 
 2. Ejemplo en Python

factorial de 5 seria:
	5 * 4 * 3 * 2 * 1  = 120
"""
 
def factorial(x,n):
	"""
	Función recursiva que calcula el factorial
	Tiene que recibir:
		x=>El ultimo valor calculado
		n=>El numero a multiplicar
	"""
	if(n>0):
		# Se va llamando a ella misma mientras el valor sea superior a 0
		x=factorial(x,n-1)
		x=x*n
	else:
		x=1
	return x
 
try:
	numero = int(raw_input("inserta un numero "))
 
	# Ejecutamos la función recusiva para el calculo
	calculo=factorial(1,numero)
	print "El factorial de %s es %s" % (numero,calculo)
except:
	print "\nTiene que ser un valor numeric

Tema 3. Arreglos

1. Arreglos unidimencionales

En Java, un arreglo es un grupo de variables (llamadas elementos o componentes) que contienen valores, todos
del mismo tipo. Recuerde que los tipos en Java se dividen en dos categorías: tipos primitivos y tipos de referencia.
Los arreglos son objetos, por lo que se consideran como tipos de referencia. Como veremos pronto, lo que
consideramos generalmente como un arreglo es en realidad una referencia a un objeto arreglo en memoria.

Ejemplo en java:

public class InicArreglo
 {
 public static void main( String args[] )
 {
 final int LONGITUD_ARREGLO = 10; // declara la constante
 int arreglo[] = new int[ LONGITUD_ARREGLO ]; // crea el arreglo

 // calcula el valor para cada elemento del arreglo
 for ( int contador = 0; contador < arreglo.length; contador++ )
 arreglo[ contador ] = 2 + 2 * contador;

 System.out.printf( "%s%8s\n", "Indice", "Valor" ); // encabezados de columnas

 // imprime el valor de cada elemento del arreglo
 for ( int contador = 0; contador < arreglo.length; contador++ )
 System.out.printf( "%5d%8d\n", contador, arreglo[ contador ] );
 } // fin de main
 } // fin de la clase InicArreglo
 
 Ejemplo en python:
 x=int(raw_input("ingrese numero: "))
for i in range(1,x+1):
	for j in range(1,11):
		print "{:>5}".format(i*j),
	print
