# Programación Básica 2


Hello there! I’m **MacDown**, the open source Markdown editor for OS X.

Let me introduce myself.


### Ejercicio 1

Dada la siguiente clase


```
public class Persona{
	private String nombre;
	private String apellido;
	
	public Persona(String nombre, String apellido){
	
		this.nombre = nombre;
		this.apellido = apellido;
	}
	
	public String getNombre(){
		return this.nombre;
	}
	
	public void setNombre(String nombre){
		this.nombre = nombre;
	}
	
	public String getApellido(){
		return this.apellido;
	}
	public void setApellido(String apellido){
		this.apellido = apellido;
	}
}
```
* Donde se observa el encapsulamiento?
* En el constructor, identificar que es una variable y que es un atributo

### Ejercicio 2

Crea una clase llamada Cuenta que tendrá los siguientes atributos: titular y
saldo, el saldo puede tener decimales.
El titular será obligatorio y la cantidad es opcional. Crea dos constructores que cumpla lo
anterior.

* Construir los siguientes métodos

```
/**
La cantidad se suma al saldo, si la cantidad
es negativa el saldo no debe ser afectado
*/
public void depositar(Double cantidad){
	//...
}
```
```
/**
Restamos cantidad al saldo actual, si la cantidada a retirar
es mayor que el saldo no se debe afectar el saldo
*/

public void retirar(Double cantidad){
	//...
}
```
* ¿Que pasa con los setters en este caso?

### Ejercicio 3

Crea la clase Persona para que cumpla 
las siguientes condiciones:

* Sus atributos son: nombre, edad, DNI, sexo (H hombre, M mujer), peso y
altura. No queremos que se accedan directamente a ellos. Piensa que
modificador de acceso es el más adecuado, también su tipo. Si quieres añadir
algún atributo puedes hacerlo.

* Por defecto, todos los atributos menos el DNI serán valores por defecto según
su tipo (0 números, cadena vacía para String, etc.). Sexo sera hombre por
defecto, usa una constante para ello.

* Debe tener los siguientes constructores:
	1. Un constructor por defecto.
	2. Un constructor con el nombre, edad y sexo, el resto por defecto.
	3. Un constructor con todos los atributos como parámetro.

* Los métodos que se implementaran son:
 
	1. calcularIMC(): calculara si la persona esta en su peso ideal (peso en
kg/(altura^2 en m)), si esta fórmula devuelve un valor menor que
20, la función devuelve un -1, si devuelve un número entre 20 y 25
(incluidos), significa que esta por debajo de su peso ideal la función
devuelve un 0 y si devuelve un valor mayor que 25 significa que
tiene sobrepeso, la función devuelve un 1. Te recomiendo que uses
constantes para devolver estos valores.

	2. esMayorDeEdad(): indica si es mayor de edad, devuelve
un booleano.

	3.  getters y setters para todos los propiedades
	 
* crear los siguientes test:

	1. Comprobar si esta en su peso ideal
	2. Tiene sobrepeso
	3. Esta por debajo de su peso ideal
	4. Si es mayor de edad
	

### Ejercicio 4

La clase​ ​Password tiene dos atributos

* longitud, por defecto tienen 8 caracteres 
* contraseña, (el string que representa la contraseña) 

Un password se considera fuert si tiene:

* ​+ ​de​ ​2​ ​mayúsculas
* ​​+ de ​ ​de​ ​1​ ​minúscula​ ​
* ​+ de​ ​5​ ​números

* Los​ ​constructores​ ​serán​ ​los​ ​siguiente:
 	1. Un​ ​constructor​ ​por​ ​defecto.
	2. Un​ ​constructor​ ​con​ ​la​ ​longitud​ ​que​ ​nosotros​ ​le​ ​pasemos.​ ​
	
* Los​ ​métodos​ ​que​ ​implementa​ ​serán:
	2. CambiarContraseña
	3. Método​ ​get​ ​para​ ​contraseña​ ​y​ ​longitud.


### Ejercicio 5

¿Cuál​ ​será​ ​el​ ​resultado​ ​de​ ​ejecutar​ ​el​ ​siguiente​ ​caso​ ​de​ ​prueba​ ​de​ ​JUnit?​ ​¿Por​ ​Qué? 

```
package​ ​ar.edu.unlam.basica2;
import​ ​static​ ​org.junit.Assert.*; 
import​ ​org.junit.Test;

public​ ​class​ ​TestString​ ​{

	@Test
	public​ ​void​ ​testIgualdadDeObjetos(){
		
		String​ ​cadena1​ ​=​ ​new​ ​String("Cadena"); 
		String​ ​cadena2​ ​=​ ​new​ ​String("Cadena");
		assertTrue(cadena1​ ​==​ ​cadena2); }
	}
```