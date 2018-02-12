# Examen-SI-401
Tema 1. Recursividad Fibonacci

La recursividad, es un concepto bastante importante y bien básico de la programación. Sin embargo es bastante difícil de asimilar 
al principio. Se supone que es algo que se va entendiendo con práctica y tiempo.
Ejemplo en java:
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
 
Ejemplo en python:
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
Tema 2.Recursividad Factorial

Ejemplo en java:

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
