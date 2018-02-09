# Examen-SI-401
recursividad
La recursividad, es un concepto bastante importante y bien básico de la programación. Sin embargo es bastante difícil de asimilar 
al principio. Se supone que es algo que se va entendiendo con práctica y tiempo.

Ejemplo:
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
 
 
 package calculofactorial;
public class PruebaFactorial{
    
public static void main( String args[] ){
    
CalculoFactorial calculoFactorial = new CalculoFactorial();
 calculoFactorial.mostrarFactoriales();
 }
 } 
