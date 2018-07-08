# Programación Básica 2


### Ejercicio 

¿Que​ ​pasa​ ​cuando​ ​se​ ​usa​ ​la​ ​palabra​ ​reservada​ ​new?​ 

¿Cual es el error en la siguiente linea? 

```
X alfredoAlcon​ ​=​ ​new​ ​Actor();;
```

### Ejercicio 

Construir la clase Rectangulo 

* Tiene dos propiedades base y altura (del tipo Double)
* Un constructor con dos parametros 
	
```
public Rectangulo(Double base, Double altura){
	//...
}

```
* Un método para calcular el area

```
/**
Calcula el area del triangulo utilizando las propiedades base
y altura
*/
public Double calcularArea(){
	//...
}

```
* Un método para calcular el perimetro

```
/**
Calcula el perímetro del rectangulo utilizando las propiedades base
y altura
*/
public Double calcularPerimetro(){
	//...
}
```
* Implementa los siguientes Tests

```
package​ ​ar.edu.unlam.basica2;
import​ ​static​ ​org.junit.Assert.*; 
import​ ​org.junit.Test;

public​ ​class RectanguloTest​ ​{

	@Test
	public​ ​void​ ​sePuedenCrearRectangulos(){
		
		Rectangulo​ ​unRectangulo​ ​=​ ​new​ ​Rectangulo(1.0, 2.0); 
		assertNotNull(unRectangulo); 
		
		Rectangulo​ ​otroRectangulo​ ​=​ ​new​ ​Rectangulo(4.0, 5.0);
		assertNotNull(otroRectangulo); 
		
		}
	}
	
	@Test
	public​ ​void​ ​elPerimetroDeUnRectanguloDebeSerLaSumaDeSusLados(){
		
		Rectangulo​ ​unRectangulo​ ​=​ ​new​ ​Rectangulo(4.0, 2.0); 
		Double esperado = 12; // 
		
		Double acual = unRectangulo.calcularPerimetro();
		
		/*
		  El tercer parametro es un delta. Quiere decir que solamente
		  nos van a importar los primeros dos decimales para la 		  comparacion
		*/
		assertEquals(esperado, actual, 0.01); 
		
		}
	}
	
	@Test
	public​ ​void​ ​elAreaDeUnRectanguloDebeSerLaBasePorSuAltura(){
		
		//
	}		
	
```


### Ejercicio 

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

### Ejercicio 

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

### Ejercicio 

Crea la clase Persona para que cumpla 
las siguientes condiciones:

* Sus atributos son: nombre, fecha de nacimiento, DNI, sexo (H hombre, M mujer), peso y
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
un booleano.<br>
***TIP***: Investigar la clase [LocalDateTime](http://www.oracle.com/technetwork/articles/java/jf14-date-time-2125367.html)
	
	3.  getters y setters para todos los propiedades
	 
* crear los siguientes test:

	1. Comprobar si esta en su peso ideal
	2. Tiene sobrepeso
	3. Esta por debajo de su peso ideal
	4. Si es mayor de edad




### Ejercicio 

La clase​ ​Password tiene dos atributos

* longitud, por defecto tienen 8 caracteres 
* clave, (el string que representa la contraseña) 

Un password se considera fuert si tiene:

* ​+ ​de​ ​2​ ​mayúsculas
* ​​+ de​ ​1​ ​minúscula​ ​
* ​+ de​ ​5​ ​números

* Los​ ​constructores​ ​serán​ ​los​ ​siguiente:
 	1. Un​ ​constructor​ ​por​ ​defecto.
	2. Un​ ​constructor​ ​con​ ​la​ ​longitud​ ​que​ ​nosotros​ ​le​ ​pasemos.​ ​
	
* Los​ ​métodos​ ​que​ ​implementa​ ​serán:
	2. CambiarContraseña
	3. Método​ ​get​ ​para​ ​la clave​ ​y​ ​longitud.

* TODO: agregar casos


### Ejercicio 

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

### Ejercicio 

Un rectangulo se define como un paralelogramo cuyos cuatro lados forman ángulos rectos entre sí. Un cuadrado es una particularidad del rectangulo donde los cuatro lados son iguales. Utilizandola clase Rectangulo que programaste antes implementa la clase Cuadrado


### Ejercicio
A partir de las clases Polinomio y Monomio te proponemos que modeles las siguientes clases usando Herenecia

1. Función constante. Es un [polinomio] donde su [grado] es 0
2. Función lineal. Es un [polinomio] donde su [grado] es 1
3. Función cuadrática. Es un [polinomio] donde su [grado] es 2

[polinomio]:https://es.wikipedia.org/wiki/Polinomio
[grado]:https://es.wikipedia.org/wiki/Polinomio#Grado_de_un_polinomio


```
/**
 * Clase que quedela un mononio.
 * Un monomio es una expresión algebraica en la que se utilizan exponentes naturales de variables literales
 * que constan de un solo término (si hubiera una suma o una resta sería un binomio),
 * un número llamado coeficiente
 * Ejemplo de un monomio
 *
 * 4X^2
 * donde 4 lo llamamos coeficiente y al 2 el exponente
 */
public class Monomio {

    /**
     * El exponente tiene que ser un numero natural (positivo)
     */
    private Integer exponente;
    private Double coeficiente;

    public Monomio(Integer exponente, Double coeficiente) {
        this.exponente = exponente;
        this.coeficiente = coeficiente;
    }

    public Double evaluar(Double x){

        return  coeficiente * Math.pow(x, this.coeficiente);
    }

}
```

```
mport java.util.Arrays;
import java.util.List;

public class Polinomio {

    private List<Monomio> monomios;

    public Polinomio(Monomio...monomio) {

        this.monomios = Arrays.asList(monomio);

    }

    public Double resolver(Double x){

        Double resultado = 0d;

        for (Monomio unMonomio: monomios) {

            resultado += unMonomio.evaluar(x);
        }

        return resultado;
    }
}
```

### Ejercicio 
La Interpretación geométrica de las sumas de Riemann explicada en este 
[link](https://ekuatio.com/calculo-de-una-integral-definida-por-las-sumas-de-riemann/) es un método para resolver las integrales. 
Implementa el método ***resolver*** y testea los siguientes casos

* f(x) = x entre 0 y 1 
* f(x) = x entre 0 y -1
* f(x) = x^3 entre -1 y 1 


```
public class IntegralRiemann {
    
    private Polinomio polinomio;

    public IntegralRiemann(Polinomio polinomio) {
        this.polinomio = polinomio;
    }
    
    public Double resolver(Integer limiteInferior, Integer limiteSuperior){
        
        Double resultado = 0d;
        
        //
        return resultado;
    }
}

```

### Ejercicio

Te​ ​proponemos​ ​realizar​ ​el​ ​modelo​ ​que​ ​permita​ ​representar​ ​distintas​ ​figuras geométricas.
Para​ ​empezar,​ ​consideremos​ ​las​ ​siguientes:

* Circulo
* Rectangulo
* Cuadrado
* Triangulo

​​​​​​​​​​Para​ ​probar​ ​que​ ​las​ ​clases​ ​que​ ​diseñaste​ ​cumplen​ ​con​ ​un​ ​funcionamiento​ ​óptimo,​ ​te sugerimos​ ​desarrollar​ ​los​ ​casos​ ​de​ ​prueba​ ​​ ​que​ ​validen​ ​lo​ ​siguiente:

1. Verifica​ ​que​ ​a​ ​partir​ ​de​ ​un​ ​mismo​ ​método,​ ​podemos​ ​dibujar​ ​cualquier​ ​figura. Por​ ​el​ ​momento​ ​sólo​ ​te​ ​conviene​ ​hacer​ ​que​ ​el​ ​método​ ​imprima​ ​el​ ​área​ ​y​ ​el​ ​perímetro​ ​de​ ​la figura.
2. Verifica​ ​que​ ​podemos​ ​dibujar​ ​un​ ​círculo​ ​con​ ​un​ ​radio​ ​de​ ​10
3. Verifica​ ​que​ ​podemos​ ​dibujar​ ​un​ ​rectángulo​ ​con​ ​un​ ​lado​ ​de​ ​10​ ​y​ ​otro​ ​de​ ​5 ​​​​​​​​​​​
4. Verifica​ ​que​ ​podemos​ ​dibujar​ ​un​ ​triángulo​ ​con​ ​los​ ​siguientes​ ​lados​ ​(10,​ ​7,7.14)​ ​y​ ​los​ ​los​ ​siguientes​ ​ángulos​ ​(90,​ ​45,​ ​45)
5. Chequá​ ​que​ ​no​ ​te​ ​permita​ ​dibujar​ ​un​ ​circulo​ ​con​ ​un​ ​radio​ ​igual​ ​a​ ​-5​​
6. ​También​ ​deberías​ ​chequear​ ​que​ ​no​ ​te​ ​permita​ ​dibujar​ ​un​ ​rectángulo​ ​con​ ​los lados​ ​10​ ​y​ ​10
7. ​Fijate​ ​que​ ​no​ ​sea​ ​posible​ ​dibujar​ ​un​ ​triángulo​ ​con​ ​los​ ​lados​ ​(10,​ ​7​ ​y​ ​7.14)​ ​para los​ ​ángulos​ ​​ ​(90,​ ​45,​ ​90)
8. Fijate​ ​que​ ​no​ ​sea​ ​posible​ ​dibujar​ ​un​ ​triangulo​ ​con​ ​los​ ​lados​ ​(10,​ ​10,​ ​30)​ ​con​ ​los
angulos​ ​(45,​ ​90,​ ​45)



### Ejercicio 

Refactorizar el metodo esFuerte() de la clase Password del ejericio x

```
public Boolean esFuerte(){

	return this.validadorMayusculas.validar(this.clave) &&
			this.validadorMinusculas.validar(this.clave) &&
	    	this.validadorNumeros.validar(this.clave) &&
}

```
Donde

* validadorMayusculas
* validadorMinusculas
* validadorNumeros

Son son instancias de clases que implementan la siguiente interfaz

```
public interface ValidadorClave{

	Boolean validar(String clave);
}

```

### Ejercicio 

Crear la clase PasswordBuilder la misma deberia poder ser usada de la siguiente forma

```
Password unPassword = new PasswordBuilder()
								.clave("unaClave")
								.agregarValidador(new ValidadorMayusculasValidator(2))
								.agregarValidador(new ValidadorMinusculassValidator(1))
								.build();
						
```

Vas a tener que: 

* Modificar la clase password para que tenga una lista de validadores
* Modificar el metodo esFuerte() para que itere la lista de validadores y los ejecute+
* Los validadores concretos deber recibir como parametro la cantidad minima aceptada

#####Ejemplo

```
ValidadorMayusculasValidator  validador = new ValidadorMayusculasValidator(2)

/*
En este caso debe devolver false porque el String que recibe como 
parametro solo tiene una mayúscula
*/
validador.validar("unClave")

```


### Ejercicio 



Posibles ejercicios

Ordenamiento
Metodos de ordenamiento Simples (burbujeo, insersion, seleccion) con un Strategy

Cifrdo
Implementar tres clases que cifren de distitnas formas
https://es.wikipedia.org/wiki/Cifrado_cl%C3%A1sico#Cifrado_por_sustituci%C3%B3n
	


Ideas, agregar ejercicios de modelado y de patrones de diseño
Necesitamos agregar tips que les sirvan para implementar test







 